# Welcome!
Welcome to Dr. Kathy Mills' Integrated Systems Ecology Lab at the Gulf of Maine Research Institute!

This repository contains a collection of documents and resources designed to support the development of individual lab members, and in doing so, create an open, effective and productive lab team.

# Getting started
## General information
* [Lab code of conduct](https://github.com/GMRI-SEL/Lab-Management/blob/master/CodeOfCoduct.md)

## New lab members to do list
* Complete the GMRI new hire checklist with Kathy
* Send an email to [Andrew](aallyn@gmri.org) from your new GMRI email to get added to the lab email list and the GMRI quant group list serv
* Register your new email on slack and get added to the lab slack channel
* Register an account with [Freed Camp](https://freedcamp.com), make a personal group and then invite Kathy to an associated project (Professional Development)
* Register an account with [Mendeley](https://www.mendeley.com/newsfeed) and get added to the lab Mendeley folders
* Set up a GitHub account and schedule a time to walk through the Git/GitHub/RStudio tutorial with Andrew

# Meetings
## Individual meetings with Kathy
This is a work in progress as we try to find scheduling options that work best for everyone.

## Weekly progress
We will use [Kristie Whitaker's weekly meetings template](https://github.com/WhitakerLab/Onboarding) to keep Kathy (and everyone else) updated on what is going on in the lab, track our own progress, and build a stronger lab team. The idea with the weekly meetings markdown file is to reflect on your work week, including who you helped, who helped you, what you accomplished, what you struggled with and what you need from Kathy or other lab members. Along with providing an update, ideally this process will support a strong, open and collaborative lab culture. Another benefit is it gives everyone time to celebrate the little victories, which can be easily overshadowed by the regular defeats that are so common in the scientific journey.

To use this system, here are step by step directions as well as a [video](https://drive.google.com/open?id=1Q4M_P75o91jeMJiplhykZlJAgz9gTldv) capturing how I did this on my machine (with additional steps that Kathy would take to add comments to lab member's weekly updates).

### Initial set up: Fork/Clone and set up upstream connection to the GMRI-SEL Lab-Management repo
1. Log in to your GitHub account
2. Search for the GMRI-SEL Lab-Management repository or use this [link](https://github.com/GMRI-SEL/Lab-Management) to open it in another browser tab.
3. While on the GMRI-SEL Lab-Management repository, hit the fork button to make a copy on your own GitHub account.
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

### Using the weekly meetings update files
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
12. **Finally, see Andrew when these instructions inevitably do not work**

## Group lab meetings
Lab meetings are scheduled for every other Wednesday from 1:00 - 2:00. For the late/spring summer, we will have lab meetings on 4/24, 5/8, 5/22, 6/5, 6/19, 7/3, 7/17, 7/31, 8/14, 8/28 in the Boulos (second floor) conference room. Andrew will send out a meeting reminder the morning of, which will also include information if you need to use zoom to connect remotely.

Have an idea for an upcoming lab meeting topic? [Add it to the list!](https://docs.google.com/document/d/1PVWt2vhLGfHVYaQJkdCamAPiajUAa-xUM5aoaydEGGk/edit)

# Helpful resources
## R
* Hadley Wickham's [R for Data Science](https://r4ds.had.co.nz) and [Advanced R](http://adv-r.had.co.nz)
* Yihui Xie (and others) [definitive guide to R Markdown](https://bookdown.org/yihui/rmarkdown/)
* rOpenSci's [package development/maintenance and peer review tips](https://ropensci.github.io/dev_guide/reviewtemplate.html)

## Git and GitHub
* Jenny Bryan's [Happy Git](https://happygitwithr.com)
* Git/GitHub/RStudio workflow(https://docs.google.com/presentation/d/1ghOk8L7cn1W1HNLOJ0282wT1FIZggFX5A2DlN3dERn4/edit?usp=sharing)

## Markdown
* Comprehensive [Markdown Guide](https://www.markdownguide.org)
* [Markdown cheat sheet](https://en.support.wordpress.com/markdown-quick-reference/)

## Writing
* [The 5 pivotal paragraphs of a paper](https://dynamicecology.wordpress.com/2016/02/24/the-5-pivotal-paragraphs-in-a-paper/)
* [How to write a great article -- act like a fiction writer](https://dynamicecology.wordpress.com/2014/06/11/how-to-write-a-great-journal-article-act-like-a-fiction-author/)
* [Tricks for clear writing](https://dynamicecology.wordpress.com/2012/11/14/clear-writing/)

# For a rainy day
* [Keep pushing](http://matt.might.net/articles/phd-school-in-pictures/) -- although referencing a PhD, this is broadly applicable




