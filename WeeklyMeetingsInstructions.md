# Weekly Meetings Instructions
We will use Git/GitHub to keep everyone up to date and support lab collaboration following 

# Instructions
## Initial set up: Fork/Clone and set up upstream connection to the GMRI-SEL Lab-Management repo
1. Log in to your GitHub account
2. Search for the GMRI-SEL Lab-Management repository or use this [link](https://github.com/GMRI-SEL/Lab-Management) to open it in another browser tab.
3. While on the GMRI-SEL Lab-Management repository page, hit the fork button to make a copy on your own GitHub account.
4. After the fork finishes, go to the "Clone or Download" button on your forked copy of the Lab-Management repo and copy the https link.
5. Open up a terminal window and navigate to where you would like to clone your Lab-Management copy. For example:
>cd ~/Box/Andrew\ Allyn/GitHub/

gets Andrew to his personal GitHub folder on the Box GMRI shared drive. A quick note here, the "\" is needed on Macs for folders with spaces in the name.
6. Once you are in the desired directory, type the following into the terminal:
>git clone *paste the https link you copied from step 4*

You should see something like "Cloning into..." if this is all working correctly.
7. Change your directory in the terminal to the Lab-Management folder you just cloned. For example:
>cd ~/Box/Andrew\ Allyn/GitHub/Lab-Management

once there, check to make sure everything was copied over by typing 
>ls 

in the terminal.
8. At this point, we have forked and cloned the GMRI-SEL Lab-Management folder and we are able to make changes and then submit pull requests to the GMRI-SEL account to incorporate our changes into the orginal repository. However, we don't have the ability to easily bring in any changes that the GMRI-SEL account makes to the original repository. For instance, if Kathy was to add some files and we did a "git pull", we wouldn't see those changes. To enable this connection, we need to establish an upstream link. To track this, start by typing 
>git remote -v

in the terminal and notice the only connections we have are to our fork/cloned copy of the GMRI-SEL Lab-Management repository.
9. Go back to your GitHub account in the browser and at the top of the page you should see something like 
*your name/Lab-Management*
and below that you should see
*forked from GMRI-SEL/Lab-Management*
click on the *forked from GMRI-SEL/Lab-Management link*
10. Now, you should be on the GMRI-SEL/Lab-Management page. Go to the "Clone  or Download" button and copy the https link.
11. Go back to the terminal, make sure you are in your Lab-Management folder and then type
>git remote add upstream *paste the link you copied from step 10*

12. To make sure this worked, type
>git remote -v

And you should now see connections to the GMRI-SEL Lab-Management account
13. In the terminal, you can now pull these changes as
>git pull upstream master --ff-only

and then push them 
>git push 

## Using the weekly meetings update files
Hopefully, you've now got everything set up so that you have forked/cloned the GMRI-SEL Lab-Management repository to your local machine and set up an upstream connection to be able to pull any changes made to the master GMRI-SEL Lab-Management repository. Now, it is time to use the system!

1. When you log into your personal GitHub account, you will see your forked copy of the Lab-Management repository. Navigate there and then go into your personal file, and click on the "Weekly-Meetings.md" file. 
2. On the right hand side, you should see an "edit" pencil. Click that and you will now be looking at a markdown formatted document. 
3. Add a new date following the syntax provided in the example
4. Copy the entry template, which runs from ### Date to ### Date. And then paste that right below "Weekly Notes" at the top of the document. 
5. Edit the ### Date using the syntax provided in the example
6. Answer the questions
7. At the bottom of the page, under "Commit Changes" enter your last name and then the date. For example, "Allyn-06032019." Then hit commit changes. 
8. Go to the homepage for your forked copy of the GMRI-SEL Lab-Management repository and at the top you should see something like "This branch is 1 commit ahead of GMRI-SEL master. Hit the "Pull request" button to the right of that message. This is where we are submitting our changes for consideration to be included into the GMRI-SEL Lab-Management master repository.
9. Unless you are Kathy, you are all done for now and can skip to step 10! Kathy will log into the GMRI-SEL GitHub account and within the Lab-Management repository, there will be a few pull requests -- one from each of us. She will merge each of these, bringing each member's weekly updates into the master GMRI-SEL Lab-Management repository. Then, she will be able to scan through our responses. Just as we edited our own markdown files, Kathy will also be able to edit the files and add comments/responses to any of our answers <using Markdown block quotes. After making these edits, she will commit the changes as "MillsComments" and then the date, for example "MillsComments-06032019."
10. Each week, before you add your new entries (step 1-8 in this section), you will want to pull any changes that have been made to the master GMRI-SEL Lab-Management repository. To do this, navigate to your cloned copy of the repository in the terminal. For example:
>cd ~/Box/Andrew\ Allyn/GitHub/Lab-Management

and then type 
>git pull upstream master --ff-only

and then 
>git push 

11. After pulling and pushing any changes, go to your GItHub account and your forked copy of the Lab-Management repository. Check out your markdown file for any of Kathy's comments and also feel free to look at other member's Weekly-Meetings.md files to see what everyone else in the lab has been up to!
12. **Finally, see Andrew when these instructions inevitably do not work!!**
