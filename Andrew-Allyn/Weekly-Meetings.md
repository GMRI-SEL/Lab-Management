### 2019
* [12 July 2019](#date-12-july-2019)
* [5 July 2019](#date-5-july-2019)
* [26 June 2019](#date-26-june-2019)
* [14 June 2019](#date-14-june-2019)
* [7 June 2019](#date-7-june-2019)
* [31 May 2019](#date-31-may-2019)
* [17 May 2019](#date-17-may-2019)
* [10 May 2019](#date-10-may-2019)
* [3 May 2019](#date-3-may-2019)

# Weekly Notes
### Date: 12 July 2019

#### Who did you help this week?

This week I helped Kyle as he continues to work through SST data and Atlantic bluefin CPUE. 

#### Who helped you this week?

This week I got help from Miguel creating a single shapefile of the lobster management zones (trying to create a map for the ME/NH inshore trawl survey), from Kathy thinking through NASA projects and links to the NEFI summer course, and from Ashley with the ME/NH inshore trawl data. 

#### What did you achieve?

* COCA draft sent along to collaborators
* Shad climate model projections all completed, ready for review by Jamie and Mike
* First two chapters of Ecological Forecasting text and project selection
* Joint Species Distribution Model -- Thorson paper review and example code

#### What did you struggle with?

* Understanding Thorson model
* Creating map of ME/NH inshore trawl survey that matches the ones they display in reports

#### What would you like to work on next week?

* Send off shad climate model projections to confirm results
* JSDM Thorson paper review for understanding and get one example species model going
* EcoForecasting class prep
* Identify upcoming potential proposals and brainstorm ideas

#### Where do you need help from Kathy?

* Bugging co-authors on COCA paper, GitHub for lab updates

#### Where do you need help from other lab members?

* I'm sure there'll be something else that comes up, like always, for now though, weekly updates!

### Date: 5 July 2019

#### Who did you help this week?

This week I helped Kyle as he continues to work through SST data and Atlantic bluefin CPUE. 

#### Who helped you this week?

This week, Matt/Linday/Mike and I got together to discuss downloading and processing netcdf files -- particularly those from climate model projections. They were all really helpful thinking through things, especially seeing what Matt has come up with as an option for using python to download/process the data. Moving forward, seems like a fun lab activity to try to write a function we can all use to efficiently work with these common data sets. I also got help from Kathy as she sent along her draft COCA methods paper comments back!

#### What did you achieve?

* COCA MS draft revisions made and then sent along to Kathy and Andy
* Climate model projections for RCP4.5 and RCP8.5 downloaded, processed, saved as raster stack

#### What did you struggle with?

* Letting the COCA MS draft go, but finally got there! 

#### What would you like to work on next week?

* COCA methods paper wrapped up and distributed to external co-authors for review
* NASA project planning ideas, paper review
* ME SeaGrant progress
* EcoForecasting School prep work
* Get Kathy all set on GitHub for weekly updates

#### Where do you need help from Kathy?

* Next week: COCA revision edits, potential EcoForecasting school projects/discussions with NASA team

#### Where do you need help from other lab members?

* Keep these weekly updates coming!

### Date: 26 June 2019

#### Who did you help this week?

Over the last week I helped Sam with his material for the REU R workshop and then helped out a few of the REU students (inside and outside of the workshop), mainly providing example code for spatial data visualization and analysis.

#### Who helped you this week?

I got help from the entire lab this week thinking through NETCDF headaches. 

#### What did you achieve?

* Executing climate data operation (cdo) tools in the terminal through RStudio and using "system" calls, which efficiently opens/re grids/crops NETCDF climate projection data.
* COCA ms revisions

#### What did you struggle with?

* NETCDF climate projection data. I was finally able to come up with a solution for acessing, subsetting, and storing NETCDF climate model projection data. This took longer than I would like to admit. I spent the better part of the week trying to get this done in R, modidying functions I had written that use the ncdf4 and raster libraries to accomplish similar tasks with the OISST data. Eventually, I hit a road block with netcdf files that had rotated lat/long grids, and yet no way of extracting the information needed (rotated lat/lon of poles) to deal with it. So, I ended up turin
* Coding time completely engulfed any writing time again.

#### What would you like to work on next week?

Next week (short week with the holiday):
* COCA MS out to co-authors by the end of the week
* Project planning
* ME SeaGrant JSDM progress

#### Where do you need help from Kathy?

* Next week: COCA revision edits

> Okay!

#### Where do you need help from other lab members?

* Give the weekly meetings update a shot
* Upcoming lab meeting topics

### Date: 14 June 2019

#### Who did you help this week?

This week I provided a basic guide to spatial data manipulation and operations to the quant group -- mainly for Kyle and Allison (REUs) after hearing they will be doing some spatial data analysis. I also helped Leigh and participated in the final learning researcher interview. Finally, I provided a video to Andy about how I work with Git/GitHub/RStudio as he begins to migrate from Matlab to R.

#### Who helped you this week?

This week Lindsay, Miguel and Kenae kept the TidyTuesday on a Thursday rolling, which was awesome! I also got help from Lindsay as I referred to her RMarkdown guide while making the spatial data manipulaiton/operations guide. 

#### What did you achieve?

* Shad project work, including getting some basic maps together additional spatial data layers we might need (jurisdictional boundaries, rivers, lakes), downloading the CMIP5 RCP85 sst projections files
* Some work for Kathy and her shelfwide analysis, including some data manipulation and map making
* Lab management stuff: Added new spatial data vingette, wrote a function to automatically establish paths to shared folders inside the Mills Lab and outside the Mills Lab

#### What did you struggle with?

* Climate data. I had spent some time working on a climate data function that would generate URLs to THREDDS servers, establish a connection to the netcdf file, and then extract the data for a specific region of interest. Of course, when I went to implement this across all ~20 models, it failed. Despite testing it on a few different sources when I originally made it, I ran into models that required authorization, or that had completely unique THREDDS URL paths. So, I just downloaded these things manually.
* Coding time completely engulfed any writing time again.

#### What would you like to work on next week?

Next week:
* Focused writing time COCA MS discussion read through and "seasonality" check in
* American shad work: get climate data cropped and aggreagated, meet with Miguel and Matt to discuss next steps
* Joint Species Distribution Modeling work -- see GitHub readme
* NASA UNSDG work -- see GitHub readme

#### Where do you need help from Kathy?

* Next week: COCA Methods MS review

#### Where do you need help from other lab members?

* Next week, may really try to get the entire lab to upload a weekly meetings update. Seems like a good time with Kathy away.

### Date: 7 June 2019

#### Who did you help this week?

This week I helped (or hopefully helped!) out the lab and Tidy Tuesday group get going, and helped out Leigh by participating in first screening of Learning Researcher candidates, which was really fun. 

#### Who helped you this week?

Everyone! A really fun week in the lab this week. Everybody was incredibly helpful during lab meeting and especially during the first Tidy Tuesday session as we all worked through things together. I also got some help from the lab on how to best go about calculating percent changes when dealing with seasonal projections. 

#### What did you achieve?

* Finished up COCA Stonington report figs and edited report code
* Finished FO review with Kathy and Matt
* Completed initial plots for Kathy and shelfwide assessment paper
* Some preliminary work reviewing ME SeaGrant and NASA proposals, outlining objectives, data sources and analysis first steps
* Beginning shad work gathering rivers shapefile and reading about air-river models
* Lab management stuff: updated welcome page, added instructions for using these weekly meeting updates and instructions to get going with Tidy Tuesday

#### What did you struggle with?

* Writing. I really need to just block off this time and not let myself code through the writing time I do have scheduled. I didn't have a lot of writing to do, but was hoping to give the COCA methods paper another run through.

#### What would you like to work on next week?

Next week looks like it will be a bit of a schmorgasboard:
* COCA MS discussion read through and "seasonality" check in
* American shad work with Kathy/Matt/Miguel
* Joint Species Distribution Modeling work -- see GitHub readme
* NASA UNSDG work -- see GitHub readme

#### Where do you need help from Kathy?

* Next week: COCA Methods MS review

#### Where do you need help from other lab members?

* Keep the momentum going with Tidy Tuesday!

#### Any other topics

This space is yours to add to as needed.

### Date: 31 May 2019

#### Who did you help this week?

This week I helped out Brian working through the Stonington community report. I also helped Lindsay by providing a couple of papers and talking through measures of species distributions.

#### Who helped you this week?

This week I got help from a couple of people on different tasks. Miguel/Lindsay/Matt/Brian all helped me try to figure out what was going on with a weird coding issue. Brian also helped me out making some figures for the community report.

#### What did you achieve?

* COCA Stonington community report figures
* Code checking
* Moving most files over to Box
* FO paper review
* Lab management tidy tuesday

#### What did you struggle with?

* Time management with the COCA report figures. I always struggle with making figures and seem to spend hours just going back and forth between RStudio and viewing the output. I should look for opportunities to streamline this process and also maybe retstrict the actual time I dedicate to making figures -- otherwise it can zap entire weeks. 

#### What would you like to work on next week?

* Lab management catch up (Tidy tuesday, FreedCamp, Git/GitHub weekly updates, slack channel)
* COCA MS discussion read through
* Joint Species Distribution Modeling work
* Future air temperature work

#### Where do you need help from Kathy?

* Next week: COCA Methods MS review, Lab management stuff (FreedCamp, GitandGitHub for weekly comments)

#### Where do you need help from other lab members?

* Tidy tuesday!
* Check in on FreedCamp/Git and GitHub/Slack -- are folks using it? Why or why not? 

#### Any other topics

This space is yours to add to as needed.

### Date: 17 May 2019

#### Who did you help this week?

I helped the lab go over a potential workflow that links Git/GitHub to RStudio Projects and GMRI's Box file management system. Everything *seems* to be working okay. 

#### Who helped you this week?

This week I got help from the other people in the lab reviewing the potential workflow. I got help from Andy and Kathy with longterm planning. Karen also helped me with setting up some folders on Box.

#### What did you achieve?

* Progress on COCA methods MS. I lost about a day of work after a random Microsoft Word crash and having to find the most recent drafts amidst an unformatted text file -- lesson learned. Only going to be writing with google docs from here on out. I have about three paragraphs left, but it's definitely ready for some other eyes on it.
* COCA community report figures
* Reviewed example vingette with lab members that shows how to work with Git/GitHub/RStudio/Box
* Long-term strategizing with Kathy and Andy


#### What did you struggle with?

* Wait for it...writing and, specifically, the discussion of the COCA methods ms. I'm not sure why this is all too surprising, as I don't write that frequently. Moving forward, going to make time to practice writing at least a few times a week, rather than just waiting for a paper or proposal. I'd also really be interested in getting a writing workshop together to hear other people's approaches to writing.

#### What would you like to work on next week?

* COCA seasonality manuscript
* Wrap up PD and long term planning stuff
* Distribute vingette to other lab members for Git/Github/Rstudio/Box
* Summer intern prep

#### Where do you need help from Kathy?

* Next week: COCA Methods MS review, PD review, long term planning stuff, summer intern prep

#### Where do you need help from other lab members?

* More of the same help experimenting and finding solutions to lab software and workflow approaches as we all try to figure out how to work together as efficiently as possible.

#### Any other topics

This space is yours to add to as needed.

### Date: 10 May 2019

#### Who did you help this week?

Mostly an isolated work week this week for me. Though, I did some experimenting tryng with Git/GitHub/RStudio/Box, which seems to be working and will hopefully be helpful when we have time to look over the example code/workflow as a lab, and participated in first round post doc interviews for Andy's NSF WARMEM project. 

#### Who helped you this week?

This week I got help from Lindsay testing out the Git/GitHub/RStudio/Box workflow and from Alex K navigating some Mac file storage weirdness. 

#### What did you achieve?

* Edited Brian's COCA community report code to work with Brad's economics model results
* Produced example economic model results treemaps for Brad/Kathy to review
* Worked on COCA methods manuscript
* Proposed Box file organization structure
* Created an example vingette to show how to work with Git/GitHub/RStudio/Box
* Drafted professional development fund application materials
* Participated in post doc interviews
* Took some time for long-term strategizing

#### What did you struggle with?

* Writing -- there appears to be a trend here

#### What would you like to work on next week?

* **GET THE COCA METHODS PAPER DRAFT COMPLETED AND BACK TO KATHY**
* COCA seasonality manuscript
* Kathy and Andy meeting
* Have lab members up to speed on Git/GitHub/RStudio/Box work

#### Where do you need help from Kathy?

* Next week: Kathy/Andy meeting, time to go over Git/GitHub and Kathy's review process of weekly progress documents
* Next two weeks: COCA methods draft reviews

#### Where do you need help from other lab members?

* More of the same help experimenting and finding solutions to lab software and workflow approaches as we all try to figure out how to work together as efficiently as possible.

#### Any other topics

This space is yours to add to as needed.

### Date: 3 May 2019

#### Who did you help this week?

This week I went over a sea surface temperature extraction code with Matt, provided a trawl data processing function to Matt and Lindsay and helped Aaron with analyzing some of their electronic monitoring data. 

#### Who helped you this week?

This week I got help from the entire mills Lab while working through how to use Git/GitHub/RStudio projects to work collaboratively and from Alex K. on generating THREDDS URLS to access climate model projections.  

#### What did you achieve?

* Produced a collection of functions to collect and process physical oceanographic data from THREDDS servers, including OISST data and CMIP5 projections
* Drafted Git/Github/RStudio workflow slides and walked through collaborative coding example with Mills Lab
* Moved COCA methods paper and seasonality manuscripts along
* Worked on some Mills Lab management things (landing page, weekly meetings template)

#### What did you struggle with?

* Finding and sticking to focused writing time

#### What would you like to work on next week?

* Re submit COCA methods paper to Kathy
* Wrap up COCA seasonality paper
* Lead Mills Lab meeting to recap GitHub progress/discuss next steps: Box file organization, function code-a-thon

#### Where do you need help from Kathy?

* Next week: COCA methods paper, Job and planning (time on ME Sea Grant, NSF WARMEM, others?)

#### Where do you need help from other lab members?

* Guidance with Box file organization/priortizing what functions we might want to write as a lab/feed back on how all of these new things are working (FreedCamp, GitHub, Weekly-meetings markdown file updates)

#### Any other topics

This space is yours to add to as needed.
