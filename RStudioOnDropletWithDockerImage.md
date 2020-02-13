
# Background
This is a quick guide for getting up and running with RStudio, Git/GitHub, Docker, GoogleDrive and DigitalOcean to support cloud computing tasks. None of it would have been possible without [Alex Kerney's](https://github.com/abkfenris) help. If you aren't at GMRI and are using this guide without acess to Alex (or another Alex), I wish you the best of luck.

A lot of what we do is not necessarily compute intensive and is easily done on our local machines. Occassionally, though, we might have an analysis that takes up a lot of time -- this could be one task that takes a really long time (e.g., fitting a Vector Autoregressive Spatio-Temporal Model to the NOAA NEFSC bottom trawl survey data for a single species) OR it could be a task that might not take much time run once, but that we need to repeat multiple times (e.g., fit the same model to many different species). When either of these situations arise, we could increase our efficiency by using cloud computing capabilities instead of our local machines and that's where RStudio, Git/GitHub, Docker, GoogleDrive and DigitalOcean come into play. This suite of applications allows us a number of key advantages, including:

1. *Actually* reproducible science. By using Git/GitHub and linking repositories to RStudio projects, we are already taking one giant step towards more reproducible science. With the addition of Docker, we are adding in another level of "reproducibility." Docker essentially builds an identical computing environment (e.g., RStudio and R version, package versions, etc) to the environment used to run our current analysis code. In other words, no more package version install issues or differences in results based on varying RStudio/R/package versions. 
2. More efficient computing. Using a combination of Docker and DigitalOcean, we can now create specific DigitalOcean "droplets" (i.e., remote servers) far superior to our personal computers and specifically alligned with our data analysis tasks. This should dramatically cut back on the time spent "waiting" for different processes to run.

Along with Alex's help, a lot of what follows comes from a combination of existing sources. In particular, I relied heavily on:
- Jenny Bryan (Git/GitHub and R): https://happygitwithr.com/
- Andrew Heiss (R, DigitalOcean, and R's "future" package): https://www.andrewheiss.com/blog/2018/07/30/disposable-supercomputer-future/
- Andrew Heiss (Docker, RStudio and DigitalOcean): https://www.andrewheiss.com/blog/2017/04/27/super-basic-practical-guide-to-docker-and-rstudio/
- Derek Powell (Docker, Git/GitHub and Docker Hub): http://www.derekmpowell.com/posts/2018/02/docker-tutorial-2/
- Joel Nitta (Docker, DigitalOcean, GitHub and GoogleDrive) (https://www.joelnitta.com/post/how-to-run-an-r-analysis-anywhere/how-to-run-an-r-analysis-anywhere/)
- Brian Hogan (Installing Docker on DigitalOcean Droplet) (https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04) 

# The steps
## Step 1: GitHub and RStudio
In this step, you are going to create a GitHub repo and then clone the repo into a new RStudio project. There's a number of great resources out there for step by step instructions. I found [Jenny Bryan's](https://happygitwithr.com/) to be the best. After setting up the RStudio project, add a folder to the Box Mills Lab folder with the identical name. We will use Box to store large files, which don't play nice with GitHub, and then use GitHub for the code storage. To facilitate this structure, try to generate paths to read or write large files using the "GenerateSharedPathsScript" function and then pasting this along with the file name. This is accomplished by adding the following line to the top of your R script: <br/> `source("https://raw.githubusercontent.com/GMRI-SEL/LabFunctionsandCode/master/GenerateSharedPathsScript.R")`  

Windows users will be prompted to enter their user name. This is the user name associated with your Box account. In other words, whatever the user name is that would complete the path to Box as `C:/Users/user.name/Box/` After sourcing this function and entering the user name (if required), you will now have a suite of stem paths in your environment, including to the lab data (lab.data.path) and lab functions (lab.func.path) folders, to the RES department data (res.data.path) and functions (res.func.path) folders, and also to the Mills Lab project folder with the identical name to the RStudio Project currently in use (proj.path). For example, if my GitHub Repo was named "Fish2020" and I generated my RStudio Project with the same name ("Fish2020) as well as a "Fish2020" folder within the Box/Mills Lab/Projects/ folder, I now have access to Box/Mills Lab/Projects/Fish2020. When reading/writing/sourcing files in these different folders, you would then just append the file name to the stem paths. For example, writing a large results csv file ("Fish2020results"), you would do: <br/>
`write.csv(Fish2020results, paste(proj.path, "Results/Fish2020results.csv", sep = ""))`

For accessing files within the repo (e.g., other code, small files), try to use the `here::here(folder.name, file.name)`structure so that paths are relative and not absolute. 

For larger files, the best approach I have found relies on Google Drive. [Joel does an excellent job explaining this and working through a few examples.](https://www.joelnitta.com/post/how-to-run-an-r-analysis-anywhere/how-to-run-an-r-analysis-anywhere/) For some more example, this is how I have gotten data off of a google drive folder ("SDM-convergence/Data/). After downloading, they are then available locally to load into R:
- `files.download<- drive_ls("SDM-convergence/Data/")` <br/>
- `for(i in seq_along(files.download$name)){` <br/>
    `drive_download(file = paste("SDM-convergence/Data/", files.download$name[i], sep = ""), overwrite = TRUE)` </br>
    `}`

For an example work flow exporting data, here is how I have saved some results. The key is to first create a zipped folder of everything you want to save and then export that zipped folder to google drive. In this case, those files are all within the "OutFile" folder
- `files2zip<- dir(OutFile, full.names = TRUE)` <br/>
- `zip(zipfile = paste(OutFile, '/Zip', sep = ""), files = files2zip)`</br>
- `drive_upload(media = paste(OutFile, "/Zip.zip", sep = ""), name = paste("NEFSC", season, gsub(" ", "", paste("_", to_any_case(spp, case = "sentence"), sep = "")), sep = ""))`

**If you go the Google Drive route, make sure to add the following lines to your .gitignore file for your GitHub repo**
- `# Ignore authorization info for access to google drive` <br/>
`.httr-oauth`

## Step 2: Code away!
Work on your analysis code on your local machine. In addition to setting up the analysis, another thing to do here is to to test whatever task you are hoping to run on the DigitalOcean droplet at a smaller scale. For example, if I was fitting a single model that takes a very long time, I might subset the data in space or time to get a general idea of whether the code will work. Or, if I was hoping to use the DigitalOcean droplet to fit multiple models for different species in parallel, I might test the code on a single species first.

### Step 2a. Parallel processing
A quick note here on parallel processing. One of the big advantages to running your analysis code on DigitalOcean droplets is we have access to servers with a high number of CPUs, opening up the opportunity to run analyses in parallel. Another way of thinking about this is let's say that you were repeating the same analysis task on a variety of species, or in a variety of different areas or at different time periods. You might do this on your local machine using a `for` loop, or better yet using one of the `apply` or `map` family of functions. These work, but what if you could send each of the loop iterations, or tasks, out to a completely different computer? You'd automatically cut down on your analysis time by a factor of the number of computers you had available. That is the idea behind the parallel processing. So long as the runs are independent, you should be good to go. [Andrew Heiss](https://www.andrewheiss.com/blog/2018/07/30/disposable-supercomputer-future/) has a few nice examples that describe this process in more detail and the [vingette from the `future` package](https://cran.r-project.org/web/packages/future/vignettes/future-1-overview.html) is also really great, too. A key thing to highlight here is that you can leverage these parallel processing opportunities on your local machine! Just make sure to leave a core or two for other tasks. 

## Step 3: Git commit and Git push your code up to GitHub 
Now that you have written a bunch of code and done some preliminary testing, you want to make sure to back it up using Git and GitHub. Even if you aren't going beyond this step, you will want to do this. Along with backing up your work, making it more reproducible and easier to collaborate with others, committing and pushing your code to GitHub will allow you to access the code (and relevant files) from anywhere, including the Docker container that you will eventually launch on the DigitalOcean droplet. Again, for best practices, check out the instructions provided by [Jenny Bryan](https://happygitwithr.com/).

## Step 4: Docker 
I'm way over my head at this step. My limited understanding is that Docker allows you to take a snapshot of your computing environment as an image and then launch that image in a container, either on your local machine, or in this case on a DigitalOcean droplet. The biggest advantage I have seen so far with this is that it completely overcomes any RStudio/R/R package versioning issues and *actually* supports reproducible science by providing everything someone would need to exactly duplicate your work when coupled with the code and necessary data files. Now, how that actually gets done is where I start to fade off. Thankfully, smarter people than me have already done a lot of this work and there are a number of Docker images that can be easily downloaded and then launched through the [Rocker project](https://www.rocker-project.org/). In addition, googling "Docker and RStudio" should return a number of hits. Beyond that, we just want to make sure that all of our Docker files are also stored within the same GitHub repo as our analysis code. Once you've checked that all is well with the building the Docker image, you will the Git commit and Git push this folder/these files to your GitHub repo. 

## Step 5: Linking GitHub repo to DockerHub and supporting automatic builds
Again, this is wading into waters over my head. But, now that you have the necessary Docker files, you are going to want to store them on DockerHub (think GitHub for Docker images). This will allow you to access the Docker image and launch the Docker container (an instance of the image) on the DigitalOcean droplet. To do this:
- Go to [DockerHub](https://hub.docker.com/) and create a new account
- Link your DockerHub account to your GitHub account following [these directions](https://success.docker.com/article/how-do-i-link-my-github-account)
- Create a new repo on DockerHub and then select automatic build from the GitHub repo for this Docker image following [the directions here](https://docs.docker.com/docker-hub/builds/). This will trigger a Docker build whenever you make changes to any of the Dockerfiles and Git commit and push them.

## Step 6: Start up a DigitalOcean droplet 
Alright, now you have your code stored on GitHub and you've got a Docker image that contains all the information to build an identical computing environment as the one you were using to run your code. Now, you want to create a DigitalOcean droplet so that you can run this code within a Docker container (instance of the Docker image) on a remote server that is better equipped to handle the analysis. To do this, you will need to:
- Go to [DigitalOcean](https://www.digitalocean.com/).
- Set up a new account if necessary and then submit a ticket to request access to all of the droplet options (some of these are likely greyed out until you do this).
- Create a new project.
- Deploy a new droplet within the new project.
    + There's a lot of different options here for configuring the droplet. In the "Choose image" piece, select the Ubuntu option. For the plan, you will need to make your selection based on necessary computing power and budget. DigitalOcean provides [a nice guide to help make these selections](https://www.digitalocean.com/docs/droplets/resources/choose-plan/).
- After you've created the Droplet, copy the droplet IP address.

## Step 7: Launch a Docker container from Docker image on DigitalOcean droplet
With the DigitalOcean droplet created, it is now time that you access and launch the Docker image you created, resulting in a Docker container on the DigitalOcean droplet. To do this, you will first establish a connection to the DigitalOcean droplet, then install Docker onto the droplet and finally run our Docker image as a container on the DigitalOcean droplet. 
- In terminal, CD to correct folder for GitHub project
- In terminal, type `ssh root@IPaddressoftheDigitalOceanDroplet` making sure to paste the IP address of your droplet that you copied in ("##step-7:-start-up-a-digitalocean-droplet")
- In terminal, run the following to install Docker on the DigitalOcean droplet
    + `sudo apt update` </br>
    + `sudo apt install apt-transport-https ca-certificates curl software-properties-common` <br/>
    + `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -` </br>
    + `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"` </br>
    + `sudo apt update` <br/>
    + `apt-cache policy docker-ce` <br/>
    + `sudo apt install docker-ce` <br/>
- In terminal, run the following to launch the Docker container of your image on the DigitalOcean droplet, adjusting `<user name>`, `<clever password>` and the `rocker/verse` Docker image as necessary, where `rocker/verse` is the name of the DockerHub repo with the Docker image you want to use
    + `docker run -d -p 8787:8787 -e USER=<user name> -e PASSWORD=<clever password> -e ROOT=true rocker/verse`
- Now, in a web browser, navigate to `http://IPaddressoftheDigitalOceanDroplet:8787`, where again you would paste the IP address of your DigitalOcean droplet. When you do that you should be taken to an RStudio server browser and prompted to enter your login information that you set above.

## Step 8: Get your code into the Docker container on Digital Ocean droplet
Now inside the Docker container on the DigitalOcean droplet, you can bring in your code/relevant files and start to run your analysis on the droplet.
- Go to your GitHub account online and copy the address of the repo that has your code/data/etc.
- Start a new project in the broswer RStudio instance and select version controlled, Git, and then add the address for the repo you just copied.
- Open up a terminal window in the browser RStudio instance and type the following to make the full connection to the GitHub repo
    + `git remote add origin https://linktotherepoyoucopied.git` <br/>
        * This should return that the remote already exists if you did the above step correctly. <br/>
    + `git config --global user.name "Your github user name"` <br/>
    + `git config --global user.email "Your github email"` <br/>
    + `git config --global user.password "Your github password"` <br/>
    + `git pull origin master` <br/>
        * This should return a message that things are already up to date. <br/>

## Step 9: Code away!
With everything set up, you can now run and work on your code as you would on your local machine. There shouldn't be any major differences here, especially if you are using the `here::here()` approach for reading/writing files within your Repo and google drive for larger files. Just make sure that you have taken steps to save your results (whether that's google drive or some other mechanism), otherwise anything you've generated will be lost when you destroy the droplet. 

## Step 10: Git commit and push any of your changes to GitHub
Assuming you've made some edits to your code or generated some new files that might be saved within folders on your repo, you now want to ensure that they aren't lost when you destroy your DigitalOcean droplet and shut down the Docker container. For code and smaller files, you can use Git commit and Git push as you normally would on your local machine. Again, see [Jenny Bryan's](https://happygitwithr.com/) instructions if you have any questions about how to do this. For larger files, I've found that using google drive is easiest, though, I'm assuming there are other options, too. 

## Step 11: Clean up
When you're all done, it's time to clean things up. First **make sure you have all the files/results you created in this analysis saved somewhere outside the Docker container!** Once you are convinced that you have access to the new files/results (whether thats on GoogleDrive or GitHub or somewhere else), now you are ready to destroy the Droplet.
- In terminal where you typed ssh root, type `exit`.
- Go back to DigitalOcean online and destroy the Droplet.

# Wrap Up
Hopefully this has been somewhat helpful. A few things I'd like to address next:
- Constructing the DigitalOcean droplet through R using the `analogsea` package
- Mounting volumes. After talking to Alex he mentioned that it would probably make the most sense to mount volumes that map local folders to folders within the Docker container. Alex does this first by editing his Docker file to include the following to first make a directory and then set that as the working directory
    - RUN mkdir -p /usr/src/app
    - WORKDIR /usr/src/app
Then within his Docker compose file he adds the following:
    -   volumes:
        - .:/usr/src/app
Which will map the home directory (.) to the "usr/src/app" directory within the Docker container. Then, you would do Git Commit and Git Push and whichever files you have added would be in your GitHub repo and you could easily Git Pull these on your local machine.

I haven't done too much of this yet. Though it looks like for most of the rocker Docker images the specify the mkdir as `/home/rstudio`. I also wonder if adhering to the `here::here()` approach for specifying file paths might accomplish the same thing? Also, for most results, I don't think we would be able to do this as GitHub is not a great place for storing large datafiles. One option might be to mount a volume to the Box folder? Then outputting results/large created data files, would be easier...maybe?