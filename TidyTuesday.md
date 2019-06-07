## Welcome to Tidy Tuesday!
### Overview
The [Tidy Tuesday](https://github.com/rfordatascience/tidytuesday) project is an effort kickstarted by the R for Data Science Community (R4DS) that provides weekly datasets for researchers to use to enhance their coding skills and build collaborations. Dr. Mills' Integrated Systems Ecology Lab participates in Tidy Tuesdays, along with other interested folks in the GMRI Research Department, *every Thursday afternoon.* As the founders describe, "the intent of Tidy Tuesday is to provide a safe and supportive forum for individuals to practice their wrangling and data visualization skills independent of drawing conclusions" [Tidy Tuesday official GitHub repository](https://github.com/rfordatascience/tidytuesday). Whether you consider yourself an expert in data manipulation and vizualization using the Tidyverse language, or if you've never seen the "%>%" operator before, all are welcome and encouraged to participate! For some great examples, just search twitter for "#tidytuesday."

### Getting started
Before doing anything, double check that you have a recent version of R and RStudio installed. Now, once you've done that there are two ways to get going. 

*Option One -- Reading in data using the https links*
1. On the [Tidy Tuesday repository page](https://github.com/rfordatascience/tidytuesday) scroll down to the "DataSets" section and then find the data set for that week, which is usually always going to be the last entry/most recent dataset. 
2. Click on the link for the data (third column) and this will bring you to a new webpage. 
3. Copy the code chuck right below "Get the data!". For example, the ramen ratings dataset would be *ramen_ratings <- readr::read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2019/2019-06-04/ramen_ratings.csv")*
4. Open RStudio and a new script. At the top of your script (and after installing the tidyverse package) type
```{r}
library(tidyverse)
ramen_ratings <- readr::read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2019/2019-06-04/ramen_ratings.csv")
```
5. Off you go! 

*Option Two -- Fork/clone and establish upstream connection to the Tidy Tuesday repository*
This is a bit more involved. However, it will likely make things a bit easier/more reproducible. Additionally, it will help increase our Git/GitHub skills and who doesn't want to do that?!

1. Log in to your GitHub account
2. Search for the Tidy Tuesday repository or use this [link](https://github.com/rfordatascience/tidytuesday) to open it in another browser tab.
3. While on the Tidy Tuesday repository page, hit the fork button to make a copy on your own GitHub account.
4. After the fork finishes, go to the "Clone or Download" button on your forked copy of the Tidy Tuesday repo and copy the https link.
5. Open up RStudio and a new project. Select the "Version Control" option and then "Git." In the "Repository URL" box, paste the link you copied in step 4. In the "Project directory name" box type "tidytuesday" and then double check the project is being created where you want it. 
6. At this point, we have forked and cloned the Tidy Tuesday repository and we are able to make changes. If we wanted, we could submit pull requests for the Tidy Tuesday account to incorporate our changes into the original repository. However, we don't have the ability to easily bring in any changes that the Tidy Tuesday account makes to the original repository. For instance, when next week's data set is added, we won't see it in our local fork/cloned repository even if we do "git pull." To enable this connection, we need to establish an upstream link. To track this, in RStudio open up a new terminal under the "Tools" tab. And then type
>git remote -v

and notice the only connections we have are to our fork/cloned copy of the Tidy Tuesday repository.
7. Go back to your GitHub account in the browser and at the top of the page you should see something like 
*your name/tidytuesday*
and below that you should see
*forked from rfordatascience/tidytuesday*
click on the *forked from rfordatascience/tidytuesday*

8. Now, you should be on the R for Data Science Tidy Tuesday page. Go to the "Clone  or Download" button and copy the https link.
9. Go back to the terminal, make sure you are in your tidy tuesday folder and then type
>git remote add upstream *paste the link you copied from step 8*

10. To make sure this worked, type
>git remote -v

And you should now see connections to the R for Data Science Tidy Tuesday account
11. In the terminal, you can now pull these changes as
>git pull upstream master --ff-only

and then push them 
>git push 

12. Off you go! You should now be able to open a new script and either load the data using the method in option 1 above, OR, since you now have a local copy on your machine, you could do something like:
```{r}
wine_ratings <- readr::read_csv(here("data", 2019/2019-06-04/ramen_ratings.csv"))
```
13. Code away, save, commit and push your changes. Before each Tidy Tuesday (on a Thursday) session, navigate to your tidy tuesday folder in the terminal and then type 
>git pull upstream master --ff-only

to get the most recent data. 

### Learning from others: David Robinson (Chief Data Scientist at DataCamp)
As we get going with this, we will work use code provided by [David Robinson](http://varianceexplained.org). This is a great opportunity to learn from an expert in the field. He even posts [live videos](https://www.youtube.com/user/safe4democracy/videos) of his analysis that you can watch! Additionally, as we will all be working from the same code rather than running into individual road blocks, it should facilitate discussion and collaboration. Though, we can certainly branch out as we progress by either starting off with a blank script, or tackling an issue that we all find interesting unrelated to the Tidy Tuesday effort. For example, we might decide to spend the Tidy Tuesday (on a Thursday) time creating a standardized and efficient function to gather, process and visualize sea surface temperature.

To use the code provided by David, again there are two options. 

*Option One -- Download David's RMarkdown script each week*
1. Navigate to [David's data screen casts repository](https://github.com/dgrtwo/data-screencasts).
2. Locate the .Rmd file you are interested in using and click on it.
3. Copy all of the text.
4. Open up a new RStudio RMarkdown file, paste the text and then save it.
5. Off you go!

*Option Two -- Fork/Clone and establish upstream connection to the David's data-screen casts repository*
1. Log in to your GitHub account
2. Search for the David's data-screencasts repository or use this [link](https://github.com/dgrtwo/data-screencasts) to open it in another browser tab.
3. While on the data-screencasts repository page, hit the fork button to make a copy on your own GitHub account.
4. After the fork finishes, go to the "Clone or Download" button on your forked copy of the data-screencasts repo and copy the https link.
5. Open up RStudio and a new project. Select the "Version Control" option and then "Git." In the "Repository URL" box, paste the link you copied in step 4. In the "Project directory name" box type "data-screencasts" and then double check the project is being created where you want it. 
6. At this point, we have forked and cloned the data-screencasts repository and we are able to make changes. If we wanted, we could submit pull requests for the data-screencasts account to incorporate our changes into the original repository. However, we don't have the ability to easily bring in any changes that the data-screencasts account makes to the original repository. For instance, when David produces his next analysis as a RMarkdown document, we won't see it in our local fork/cloned repository even if we do "git pull." To enable this connection, we need to establish an upstream link. To track this, in RStudio open up a new terminal under the "Tools" tab. And then type
>git remote -v

and notice the only connections we have are to our fork/cloned copy of the data-screencasts repository.
7. Go back to your GitHub account in the browser and at the top of the page you should see something like 
*your name/data-screencasts*
and below that you should see
*forked from dgrtwo/data-screencasts*
click on the *forked from dgrtwo/data-screencasts*
8. Now, you should be on David's data-screencasts page. Go to the "Clone  or Download" button and copy the https link.
9. Go back to the terminal, make sure you are in your data-screencasts folder and then type
>git remote add upstream *paste the link you copied from step 8*

10. To make sure this worked, type
>git remote -v

And you should now see connections to David's data-screencasts account
11. In the terminal, you can now pull these changes as
>git pull upstream master --ff-only

and then push them 
>git push 

12. Now, how you use his RMarkdown files is up to you. You could just keep working within the data-screencasts RProject as the code is going to read the data from the URL link. Alternatively, within your tidytuesday RStudio project, you could open up David's RMarkdown file and save it in a tidytuesday code folder. This would then allow you to edit David's file when he reads in the data and use the "here" functionality, as 
```{r}
wine_ratings <- readr::read_csv(here("data", 2019/2019-06-04/ramen_ratings.csv"))
```
13. Code away, save, commit and push your changes. Before each Tidy Tuesday (on a Thursday) session, navigate to your tidy tuesday folder in the terminal and then type 
>git pull upstream master --ff-only

to get the most recent data. Then, change directory to your data-screencasts folder in the terminal and type
>git pull upstream master --ff-only

to get David's most recent RMarkdown analysis file.

