### 2019
#### May
* [03 May 2019](#date-03-may-2019)
* [10 May 2019](#date-10-may-2019)
* [17 May 2019](#date-17-may-2019)
* [24 May 2019](#date-24-may-2019)
* [31 May 2019](#date-31-may-2019)
#### June
* [07 June 2019](#date-07-june-2019)
* [14 June 2019](#date-14-june-2019)
* [21 June 2019](#date-21-june-2019)
* [28 June 2019](#date-28-june-2019)
#### July
* [05 July 2019](#date-05-july-2019)
* [12 July 2019](#date-12-july-2019)
* [19 July 2019](#date-19-july-2019)
* [26 July 2019](#date-26-july-2019)
#### August
* [02 August 2019](#date-02-august-2019)
* [09 August 2019](#date-09-august-2019)
* [23 August 2019](#date-23-august-2019)
#### September
* [13 September 2019](#date-13-september-2019)
* [20 September 2019](#date-20-september-2019)
* [27 September 2019](#date-27-september-2019)
#### October
* [04 October 2019](#date-04-october-2019)
* [18 October 2019](#date-18-october-2019)
#### November
* [01 November 2019](#date-01-november-2019)
* [08 November 2019](#date-08-november-2019)
* [22 November 2019](#date-22-november-2019)

# Weekly Notes

### Date: 22 November 2019

#### Who did you help this week?

I helped Miguel with trawl data processing code and associated length data problems. 

#### Who helped you this week?

* Alex helped me with some web-scraping endeavors in an effort to scrape K and L∞ from FishBase.

#### What did you achieve?

*Trawl*

* Fixed newly found errors in trawl-processing code that related to duplicate length entries and updated all previous analyses I had done with the old processing
* Wrote code to create a "long" trawl dataset by "uncounting" NLEN
* Tracked down VBGF parameters for all trawl fish species (K, L∞, Lmaturity, and Tmax) and compiled into a single table
* Calculated VBG curve for all possible species and used age-at-length estimations to group into size class by age
* Calculated percentile based size classes
* Compared viability of using age-based size classes vs percentile-based size classes
* Plotted size-class spatial/latitudinal distribution 

*VTR*

* Calculated differenced and non-differenced data correlations

#### What did you struggle with?

I struggled to decide what the best method is for creating size-classes that would be biologically meaningful. Unfortunately, though classes based on age-at-length estimation seem much more biologically relevant, percentiles are so much clean/clearer to work with. 

#### What would you like to work on next week?

Continue working on size-based analysis and read some papers to gain a better understanding of what this might look like.  


------


### Date: 08 November 2019

#### Who did you help this week?

Facilitated salmon group discussion about abstract-planning.

#### Who helped you this week?

* Andrew sent me templates for applying to the PD fund.
* Ben Tupper helped me understand intricacies of the MaxEnt models more completely, Ben also offered to put on a "package-making" workshop for the quant group if we are interested (WE ARE INTERESTED!) 

#### What did you achieve?

*Trawl*

* Created the map Kathy suggested with colored points for observations within each percecntile by decade, also added a countour layer to visualize the shifts in edges
* Redid my original latitude percentile time series plots with the updated biomass-weighted percentiles (90,95), also added the biomass-weighted centroid to that plot, used the the same color scheme as the histogram
* Create the centroid slope table Kathy suggested
* Conducted pairwise comparisons of north, south, and center slopes for all species
* Updated PowerPoint with new figures and descriptions

*Other*

* Prepared PD Fund application and researched workshop attendance budget
* Attended temperature and sea-level rise talks at GoM2050
* Attended Ben/Nick Record's talk at the Portland UseR Group

#### What did you struggle with?

I struggled a little this week because in my latitudinal accumuluation script I've written a bunch of plotting code that takes forever to run. I've now saved into pdfs or lists what I need, so I won't have to always run those chunks, but I do need to get better about keeping scripts shorter and not overusing loops. 

#### What would you like to work on next week?

This week I focused on the trawl data/lat accumulation stuff and I completed all the objectives that came out of my meeting with Kathy. I might add on an overlap analysis using density kernels to quantify shifts. Next week I will start on the updates to the VTR analysis. 


------

### Date: 01 November 2019

#### Who did you help this week?

* I edited the references section of the COCA proposal for Lisa. 
* I talked to two third grade students about microplastics. 
* I attended the Modeling Change event and remade a few of the figures for that talk. 

#### Who helped you this week?

Miguel found the the NMFS statistical areas shapefile for me. 

#### What did you achieve?

*Trawl*

* Refined biomass-weighted percentiles of major species
* Calculated the percentage of total biomass within each percentile by decade
* Plotted percent [above and below the center](https://rpubs.com/lgcarlson/trawllataccumulation) of each species' distribution by decade
* Calculated change in percent above and below the center 

*Other*

* Edits of COCA proposal
* Wrote review reflection
* Modelling change figures
* Submitted Ecosphere review
* Created powerpoint to present trawl/vtr results to Kathy

#### What did you struggle with?

Figuring out where to go next with latitudinal accumulation analysis next

#### What would you like to work on next week?

Continue with latitudinal accumulation and VTR analyses. Revisit salmon paper and write abstract for the salmon meeting. 


------

### Date: 18 October 2019

#### Who did you help this week?

I found the code to wrap strip text in facets for Andrew. I also helped Zach with some ggplot code.

#### Who helped you this week?

Alex gave us a great presentation on the horrors that can arise from mixing Box and Git. 

#### What did you achieve?

*Salmon*

* Searched for Carlin-tagged salmon scales among DMR scale samples
* Organized, double-checked, put in order, and added necessary labelling to Carlin scales in preperation for handoff to Brandon
* Created a datasheet for Brandon that contains all necessary identifying information for each sample, but excluding individuals for which there was no scale collected
* Tried to figure out why DMR database does not include any Carlin-tagged scales collected before 1978... failed. 

*VTR*

* Continued with VTR vs trawl centroid analysis
* Mapped overlap, convergence of state centroids
* Conducted [pairwise comparisons of VTR vs trawl centroid trends](https://rpubs.com/lgcarlson/vtrcentroid)
* Conducted multiple comparisons of state level centroids by species

#### What did you struggle with?

I could not figure out why the 1977 scales I pulled are not in the DMR database, but they are in the Carlin datafile. Unfortunately, I don't think *anyone* knows the answer to this question.

#### What would you like to work on next week?

Next week I will deliver the scales to Brandon and Ruth while they're in town. I will continue working on the VTR data, and I will revisit the trawl data in light of Kathy's ideal to assess biomass accumulation by latitude. I look forward to a good discussion of mixed models at lab meeting. I also need to log my mileage from my trips to Orono. Maybe we can also re-instate Tidy Thursday.


------
### Date: 04 October 2019

#### What did you achieve?

*Salmon*

* Revisited temporal trends in growth data, including adding summaries of changepoint analysis and chronological clustering to ppt
* Recreated spatial trends in growth figures with only FS, FW, PS, and marine increments
* Created mark-recapture powerpoint to present to Tim re: survival analysis
* Created encounter histories for river-recap salmon
* Revised the annulus formation presentation for meeting with Brandon and Ruth (Box\Mills Lab\Projects\Atlantic salmon\Presentations\Carlin_annulus_formation_LGC.pptx)

*VTR*

* Plotted center of [VFR biomass versus trawl biomass at survey-level](http://rpubs.com/lgcarlson/vfrcentroid)
* Read papers Kathy sent

#### What did you struggle with?

* Had issues with Box/MARK Gui synching
* Ran into more questions about the survival analysis that we need to ask Tim before we proceed
* Discouraged by outcome of LICCI proposal

#### What would you like to work on next week?

* Hopefully picking up/dropping off scales?
* Continuing to work on the VFR centroid stuff, might need additional data from Brian/Andrew/Kathy?


------


### Date: 27 September 2019

#### What did you achieve?

*Salmon*

* Explored the possibility of calculating an annulus "start" date in addition to the annulus completion date. 
* Integrated Carlin database with multiple tables from the DMR database to create a final table of 2SW river-recapture scale analysis candidates. Only 424 fish are available, assuming we can find them. Text mining of DMR tables. 
* Did changepoint analysis for first year at sea growth incrments using package bcp for [Bayesian change points](http://rpubs.com/lgcarlson/carlinBCP)
* Explored chronological clustering for growth increments


#### What did you struggle with?

* I struggled with the figuring out when the annulus formation "starts" because when looking at the circulus spacings, there isn't a clear difference in the spacings  of "summer" and "winter" circuli. The winter minimum could occur anywhere within the annulus, and the annulus marked by the observer only tells us where the annulus "ends." Because there is such a small difference between spacings of "summer" versus "winter" circuli, its not clear how we could determine which circuli are associated with the annulus. 
* I used a few changepoint methods, and none of them were able to distinguish a changepoint within the time series of the mean growth increments. I eventually stuck with the bcp because the probability distributuion around the changepoint location was helpful for me. 
* I was also not able to glean any insights of interest from the chronological clustering. I think, with the 1SW marine recaps at least, there just aren't very substantial temporal changes. 

#### What would you like to work on next week?

* Hopefully talking to Ruth and Brandon
* Hopefully picking up/dropping off scales?
* Discuss with Kathy which questions (other salmon questions that we've discussed but ranked lower in priority vs trawl)

The other salmon questions I have written down are: 
* marine survival of 2yo vs 3yo hatchery smolt using mark-recapture
* placing salmon in space/time to model thermal environment experienced
* comparison with Penobscot data (I can't remember what exactly this entailed)
* temporal changes in marine-recap salmon growth (I've already investigated this fairly thoroughly)


------


### Date: 20 September 2019

#### Who did you help this week?

I attended the meeting with the SAC/technical staff this week. Hopefully the great ideas and well-spoken opinions expressed by everyone in attendance will be heard and put into action by the managment and improve the workplace for all of us. 

#### Who helped you this week?

Tim took some time to talk to me about Greenlandic fisheries and traditional ecological knowledge. Dorothy Dankel also took the time to talk to me about her work with social ecological systems, her career path, her opinions on scientists' role in media/social media/politics. It was a great conversation that I learned so much from, and I feel extremely lucky to have had a chance to talk with her for so long! (Jeg elsker Norge!)

#### What did you achieve?

*Salmon*

* I put together a presentation on my most recent salmon findings for our meeting with Tim
* I did back-calculations with alternate deposition rates to determine FMC estimation inaccuracy
* I started writing the methods for the annulus formation paper
* I created a master-list of usable river-recaps to pull for Brandon to analyze

*Trawl*

* Dug back into trawl literature and annotated the paper we'll discuss in next week's lab meeting

*LICCI*

* Had my interview for the LICCI project on Tuesday.

#### What did you struggle with?

Getting things done amidst the many meetings this week.

#### What would you like to work on next week?

1 Acquiring and delivering scales to Brandon
2 Exploring additional suggestions re: annulus analysis from Kathy/Tim
3 Continuing to write methods, possibly introduction, since results will now be changing


------


### Date: 13 September 2019

#### Who did you help this week?

I just tried not to infect anyone with my cold this week!

#### Who helped you this week?

Mike helped me talk through my concerns about using a constant growth rate. Andrew sent me a great paper. 

#### What did you achieve?

*Salmon*

* I figured out when Atlantic salmon form their annulus! It was pretty simple to use the known dates just do some algebra. How did we not think of this before?
* I backcalculated FMC date to ensure that they were matching up with the known dates, especially important for 0SW fish. 
* I calculated the month of minimum temperature in the South Labrador blocks over time. 
* I plotted the relationship between annulus date and month of min temperature. 
* I did a thorough [literature review](https://docs.google.com/document/d/167_9ZsFspZMpZNRQ9nWdH1HiMWHdP-sd0bnh7_4jib8/edit?usp=sharing) on annulus formation date for salmonids. 

#### What did you struggle with?

Containing my excitement re: annulus formation date knowledge. 

#### What would you like to work on next week?

Presenting annulus formation date analysis to Tim, shoring up analysis, starting to write?

------

### Date: 23 August 2019

#### Who did you help this week?

Put together DFO maps for Tim. 

#### Who helped you this week?

Miguel tried to load JSON and KML files into QGIS for me after they wouldn't work in R.

#### What did you achieve?

*Salmon*

* Scale dynamics [literature review](https://docs.google.com/document/d/1f2sQ_-z2jRf9412M7dTlxMjl3DQa5dBBqyUR0Sbk8-U/edit?usp=sharing): papers I've found and papers we discussed with Tim
* Found and removed scales with impossible days at sea versus annulus combinatings
* Pulled original dataset to evaluate confidence in "end" dates
* Started [scale dynamics investigation](http://rpubs.com/lgcarlson/scaledynamics) (8-12 days/circulus)
* Updated catch per unit effort calculations of DFO data to include fathoms/net in CPUE
* Created maps of DFO data for Tim's collaborator's proposal

#### What did you struggle with?

I could not get the JSON and KMZ files that I pulled to make the DFO map to open in R or QGIS. I solved the problem by making my own shapefiles by drawing them in Google Earth based on the KMZ file that you could only open in Google Earth Pro. 

#### What would you like to work on next week?

Continue with scale dynamics investigation. Calculate minimum SST day for Labrador. Present at NADS!

------


### Date: 09 August 2019

#### Who did you help this week?

Gave Allie some recommendations for her presentation.

#### Who helped you this week?

Miguel took charge of organizing a Mendeley folder for our salmon lit review.

#### What did you achieve?

*Salmon*

* Completed and summarized the salmon [meta-analysis](https://docs.google.com/document/d/1urPFtigYs4WttConMmAtD5jK_WtxAaZ88gzbNxKFHgE/edit?usp=sharing)
* Correlations between growth increment and productivity/survial 
* Calculated mean monthly temps in each salmon migration area
* Reviewed Maxent publications to devise strategy for DFO analysis
* Created working "summer" [SDM](https://rpubs.com/lgcarlson/maxentDFO) based on DFO data

#### What did you struggle with?

I struggled to get the maxent model working and eventually had to add another environmental variable, but neither bathymetry nor calanus is especially helpful. 

#### What would you like to work on next week?

Complete maxent model for each season. Summarize past analyses for Tim's visit.

------


### Date: 02 August 2019

#### Who did you help this week?

Helped answer some tidyverse questions for Graham and Allie.

#### Who helped you this week?
 
Miguel and I had a really good discussion about a priori model selection for the salmon analyses.

#### What did you achieve?

*Salmon*

* I added some temperature exploration to the [DFO data analysis](http://rpubs.com/lgcarlson/dfodistribution)
* Began putting together salmon migration "meta-analysis" in shared Google doc

*Trawl*

* Did a few more revisions to the trawl cleaning code
* Worked on defining length relationships, thinking about how to use sized-based approached
* Read a few papers on size-based approaches to community ecology questions
* Worked on species richness by area model

#### What did you struggle with?

I struggled to find papers that used a size-based approach for a similar question, but Kathy informed me that that's probably because there aren't any!

#### What would you like to work on next week?

Next week, I'll continue working on the salmon migration meta-analysis, I'll do the survival/increment correlations, and I'll put together a synthesis of the trawl findings for Kathy. 

#### Where do you need help from Kathy?

It would be great to for us to meet with Andrew re: the leading/trailing edge question.

#### Where do you need help from other lab members?

Mike, Miguel, and I are going to work on the salmon analysis together. 

------


### Date: 26 July 2019

#### Who did you help this week?

I sat in on the Sustainable Seafood project manager all-staff interviews and provided feedback about the candidates.

#### Who helped you this week?
 
Kanae and I had a really great discussion about the role of traditional ecological knowledge in documenting climate change impacts.

#### What did you achieve?

*Salmon*

This week, I mostly worked on the [DFO dataset](http://rpubs.com/lgcarlson/dfodistribution):

* Looked at catch per 1 x 1 lat/long block
* Created utilization distribution kernels for each month
* Calculated salmon/hour effort in each lat long block
* Plotted monthly mean surface temperature recorded in each block by the fisherman
* Looked at the correlation between salmon/hour effort and SST

*Trawl*

* Made Kathy's suggested changes to the trawl cleaning code
* Started investigating length/space relationships
* Species richness model data wrangling

#### What did you struggle with?

I was under the impression that the DFO dataset was "presence only", but that is not quite the case. I would definitely like to understand more about how this data was collected, study design, sampling effort, etc. 

#### What would you like to work on next week?

I think as a salmon group, we should make some decisions about which months/migration areas are relevant to salmon in our datasets so we can start narrowing down which model parameters make sense. I think we can do this based on what I've found from the Carlin dataset and the DFO dataset. 

------


### Date: 19 July 2019

#### Who did you help this week?

I put together a Tidy Tuesday Rmd using the forecast package.

#### Who helped you this week?
 
Mike pointed out a solution to improve my GAM of lat ~ days at sea model.

#### What did you achieve?

*Salmon*

* Calculated number of days at sea for all Carlin-tagged salmon, not just those with scales collected
* Used GAM to model [latitude of recapture/return ~ days at sea](http://rpubs.com/lgcarlson/daysatseaGAM)
* Explored the effect of adding interaction terms for sea age
* Explored days at sea ~ s(lat,long), not as successful as I'd hoped
* Created a map of monthly centroid encounter locations for all Carlin-tagged salmon to better understand movement patterns/narrow down which migration areas we should be considering for each month

*Trawl*

* Revamped trawl cleaning code
* Remade centroid lat/long code/figures in [tidyverse/ggplot](https://rpubs.com/lgcarlson/tidycleantrawl)
* Began investigating fish lengths, added weighted mean for length
* Investigated bottom depths in survey area
* Thought about how to quantify spatial distribution, explored the idea of 1x1 lat/long blocks

#### What did you struggle with?

* The GAM I made does a good job, so long as you know how many days the fish has been at sea. I think to apply this to Mike/Miguel's data, we'll need to come up with a method to estimate number of days at sea based on number of circuli. 

#### What would you like to work on next week?

* Addressing Kathy's comments about trawl cleaning code and exploring ideas discussed in meeting with Tim.
* Learning more about understanding/interpreting GAMS


------

### Date: 12 July 2019

#### Who did you help this week?
 
I answered tidyverse questions for a few labmates.

#### Who helped you this week?
 
Mike and Miguel helped me talk through a few strange things I was seeing in the salmon increment data.

#### What did you achieve?

*Salmon*

* Put together a slideshow for Tim's visit summarizing what I've done so far on the Carlin data
* Re-did increment vs migration area SST models with annual anomaly rather than raw SST
* Revisited sea age classifications, quantified number of post-annulus circuli for each fish
* Found erroneous sea age classifications
* Modeled relationship between [emigration date and post-smolt/marine growth](http://rpubs.com/lgcarlson/seaageEDA)
* Searched for Newfoundland fishery logs 

#### What did you struggle with?

* After the discussion with Tim, I'm definitely left unsure about what date I should use as the annulus formation date. It sounds like people think it could be anywhere between December and June. I think the idea of using the coldest SST date is a good idea, but this requires us deciding which areas to consider. 

#### What would you like to work on next week?

Further work on picking out most important months for SST modelling.

#### Where do you need help from Kathy?

I can't specifically think of anything. 

#### Where do you need help from other lab members?

It would be fun to talk more about a Google trends paper ideas!

------

### Date: 05 July 2019

#### Who did you help this week?
 
I shared the growth marker ~ SST lm code with Miguel. 

#### Who helped you this week?
 
Matt showed the lab how he used Python to grab large, annoying datasets online.  

#### What did you achieve?

*Salmon*

* Finished growth marker ~ SST lm code
* Used Miguel's spatial correlation code to visualize spatial relationships for each growth marker
* Calculated [correlation](https://rpubs.com/lgcarlson/sstxgrowthEDA) between entire North Atlantic SST and each migration area
* Calculated correlation between Station 27 0m data and Newfoundland ERSST
* Began creating brief presentation to show Tim monthly growth rate and beginning SST findings

*Other*

* Did more GAM reading.


#### What did you struggle with?

* Miguel and I had a long discussion about using the annulus versus the winter minimum for calculating my monthly growth rates. It seems like using the minimum is the way to go, but the minimum would be the algorithm calculated and the annulus would be the human marked. Sounds like a question for Tim. 

#### What would you like to work on next week?

Further work on picking out most important months for SST modelling. Further learning about GAMs.

#### Where do you need help from Kathy?

I can't specifically think of anything. 

#### Where do you need help from other lab members?

Miguel, Mike and I should have another salmon group meeting/game plan session. 

------

### Date: 28 June 2019

#### Who did you help this week?
 
I spent some time helping Allie and Graham with various coding problems. 

#### Who helped you this week?
 
Miguel created a N Atlantic shapefile and wrote a cool spatial correlation code for SST and growth markers. 

#### What did you achieve?

*Salmon*

* Miguel and I came up with a SST gameplan. 
* I started writing growth marker ~ SST lms to get a basic understanding of growth marker relationships with N Atlantic and migration area SST means. 

*Trawl*

*  Wrote a cleaning code for the trawl surveys and updated my faulty histograms. 

*Other*

* Spent Friday doing Datacamp and learning about purrr and GAMs. 


#### What did you struggle with?

* Miguel and I were both a little overwhelmed by the many directions you could go with the salmon ERSST analysis, but I think after some struggle, we came up with a good gameplan. 

#### What would you like to work on next week?

* Continue visualizing growth marker SST relationships. Expand upon modeling/hypothesis testing. Make decisions about which migration areas/months are most valuable to include in final models. 

* Continue learning about GAMs. 


#### Where do you need help from Kathy?

*  Nothing! Enjoy your vacation! 

#### Where do you need help from other lab members?

*  Miguel, Mike and I should have another salmon group meeting/game plan session. 

------



### Date: 21 June 2019

#### Who did you help this week?
 
I put together the "Intro to Tidyverse workshop" and wrote a code to work through as a group.

#### Who helped you this week?
 
Miguel helped me translate some tidy code to base code. He also updated the ERSST code for me!

#### What did you achieve?

*Salmon*

* I located the [Station 27](https://rpubs.com/lgcarlson/station27data) data that Kathy and I talked about last week. Despite the funny file format, I was able to pull this data and begin working with it. It contains temperature measurements at multiple depths as well as salinity and density. 
* I got the ERSST data from Miguel and began looking at that as well. 

*Trawl*

*  Did some reading and created visualizations to better understand the [sampling design](https://rpubs.com/lgcarlson/trawlsummary). Worked on cleaning data. 

*Other*

* Put together the [Intro to Tidyverse](https://rpubs.com/lgcarlson/tidyverseminiworkshop) workshop and GitHub repository.


#### What did you struggle with?

* I am not 100% sure what the best method for incorporating the temperature/etc data. 

#### What would you like to work on next week?

* Creating individual "environmental profiles" that each fish likely experienced. 

* Further work on cleaning trawl data. 


#### Where do you need help from Kathy?

*  It would be great to meet again before Kathy is on vacation. 

#### Where do you need help from other lab members?

*  I think it would be a good idea plan our next quant group meeting. 

------


### Date: 14 June 2019

#### Who did you help this week?
 
I organized this week's Tidy Tuesday and showed Allison how to access the Lab Management GitHub and edit her "Weekly-Meetings.md" file. 

#### Who helped you this week?
 
Mike initiated a "salmon" meeting to discuss similarities among our datasets, our project goals, and methods we should keep consistent among analyses. It was nice to all sit down together, brainstorm, and make sure we're on the same page.  

#### What did you achieve?

*Salmon*

* Calculated the "actual" dates for monthly growth increments. Now we can tie "Month 3 at sea" to a specific date (and potentially approximate location. This will be important when pulling in environmental variables. 
* I looked at the [correlation between productivity/abundance estimates](http://rpubs.com/lgcarlson/monthlygrowthcorrelation) and monthly growth increments over time. Unfortunately, these datasets only overlap by 14 years.
* I learned how to use the "psycho" package to quickly standardize num vars.
* I learned how to use fuzzyjoin::fuzzyjoin() and tibble::tribble() to easily create new cat vars.

*Trawl*

*  Calculated and visualed [potential leading/trailing edges](http://rpubs.com/lgcarlson/trawledafigs) when considering 1%, 5%, and 10% of biomass as "edge."
* Calculated latidunal [differences](http://rpubs.com/lgcarlson/trawlleadtraileda) between 1%, 5%, and 10% "edges". 


#### What did you struggle with?

* Realized that trends in trawl dataset wasn't making sense because it needed cleaning pre-analysis.

#### What would you like to work on next week?

* I will acquire SST data for salmon "areas of interest" and look for salinity/density data from Station 27 and any other sources. 
* I will evaluate correlation between SST and zooplankton model. 
* I will prepare for Intro to Tidyverse mini-workshop.

#### Where do you need help from Kathy?

*  Kathy was going to send me the data cleaning code for the trawl data. 

#### Where do you need help from other lab members?

*  Miguel graciously offered to translate some tidy code to its "base" equivalent, and I definitely will take him up on that!

------

### Date: 07 June 2019

#### Who did you help this week?

I updated my "Intro to Markdown" document to include examples from Tidy Tuesday and shared it with the quant group via slack. I also put it on [GitHub](https://github.com/LGCarlson/Lab-Markdown-Intro/blob/master/Tidy_Tuesday_Markdown_06042019.Rmd). This week at Tidy Tuesday, I was able to share my knowledge and hopefully help other lab members understand the tidyverse commands better.   

#### Who helped you this week?

Matt shared his Shiny code, and its really helpful to have a familiar working example like that.  

#### What did you achieve?

*Salmon*

* Visualed time series of [monthly growth increment](https://rpubs.com/lgcarlson/monthlygrowthlong).
* Broke growth down into "seasonal increments" and visualized those time series.
* Used Carlin dataset to create figures similar to Fig 7 in [McCarthy, Friedland, and Hansen 2008](https://doi.org/10.1111/j.1095-8649.2008.01820.x). 

*Trawl*

* Investigated problem of extremely large biomass values for 1990s and 2000s/extermely low biomass for 2010s by creating histograms of tows per year, total biomass per year, biomass/tow per year. Found that tow per year is consistent until 2009, where it nearly doubles. Therefore, the number of tows is not skewing the 1990s/2000s biomass, but faulty biomass adjustment may be responsible for 2010s discrepancies. 
* Plotted 90, 95, 99 percentile of [latitude distribution](https://rpubs.com/lgcarlson/trawledafigs) for each species. 

*Other*

* Completed vessel safety training and learned how to do survival suit formations! 
* Tidy Tuesday for Ramen Data


#### What did you struggle with?

* Nothing specifically, just accomplishing all of the many things I hoped to get done with such a busy week of extracurriculars (intern meetings, vessel safety, quant group). 

#### What would you like to work on next week?

* As Kathy and I discussed in our meeting Wednesday, I will look at the relationship between salmon productivity/abundance and the monthly growth increments I calculated. 

#### Where do you need help from Kathy?

* It will be good to reconvene and discuss defining leading/trailing edges. This might be a good thing to loop in Andrew on. 
* Kathy is going to contact folks at NOAA about the concerning biomass trends in the trawl data. 

#### Where do you need help from other lab members?

* I would definitely like to keep Tidy Tuesday/Thursday going! 
------



### Date: 31 May 2019

#### Who did you help this week?

I dug into the documentation for dplyr::nest() when Andrew was having difficulties with it. I didn't solve his problem, but I sure tried!  

#### Who helped you this week?

Andrew sent me some leading/trailing edge papers, and we talked a little about how you could define leading/trailing edges quantitatively. 

#### What did you achieve?

*Salmon*

* I finished loop to assign growth period/monthly growth increments.
* Calculated "early growth" [growth rates](https://rpubs.com/lgcarlson/monthlygrowthlong).

*Trawl*

* Wrote loop to save the (many) species density plots to PDF, picked out the seemingly most interesting to [discuss with Kathy](https://docs.google.com/presentation/d/1LRz5f86rx5A9Pk98QLI72aoYjNMYzEVd4zivEsc8T0E/edit?usp=sharing).
* Did more reading about leading/trailing edges. I still haven't found a paper that provides a quantitiative definition. The closest thing I found in the supplementary information of a meta-analysis by [Poloczanska et al. 2013](https://media.nature.com/original/nature-assets/nclimate/journal/v3/n10/extref/nclimate1958-s1.pdf):

>We classified each observation as leading edge (n=111), trailing edge (n=106) or centre (n=105). Centre of distribution encompassed any observations that were not leading or trailing edge e.g. abundance centre, mean latitude of occurrence. Leading edges were not restricted to the poleward edge of a distribution but were taken as any section at the edge of the distribution where it is likely that distribution may be moderated by cooler waters beyond the distributional edge. For example, expansions of intertidal invertebrates eastwards along the English Channel towards the colder North Sea were classified as leading edge expansions. Similarly, equatorward range shifts of flatfish in the southern North Sea were also classified as leading edge as the species were previously excluded from these waters by cold winter temperatures. Conversely, trailing range edges were taken as locations where it is possible that distributions may be constrained by warmer temperatures beyond the range edge. Changes in range edges were calculated as the average of all observed shifts,  including no change observations.

*Other*

* Spent some time beginning to learn Shiny tools to prepare for our group coding session next week.


#### What did you struggle with?

* I struggled to find any description of how to define/calculate a leading/trailing edge. 

#### What would you like to work on next week?

* I need to figure out next steps for both salmon and trawl analyses. 

#### Where do you need help from Kathy?

* It will be good to reconvene and discuss defining leading/trailing edges. This might be a good thing to loop in Andrew on.    

#### Where do you need help from other lab members?

* We had further discussion about workflow/files organization in the shared Box folders. I'm still not sure how the trawl/Pew project fits in to everything, so I might need some help figuring out the best home for that work. 
------


### Date: 24 May 2019

#### Who did you help this week?

I put together a RMarkdown "how to" document and example and put it on GitHub so everyone can access it easily. 

#### Who helped you this week?

Miguel and I had a really good discussion about the zooplankton dataset we are working to incorporate into the salmon work. 
Kathy generously picked up my IKEA furniture and brought it to Portland! 

#### What did you achieve?

* I worked on code to assign growth increment values to each month using monthly growth models I wrote last week. 
* I used Kathy's code to calculate the center of biomass for each species, I rewrote some of the data wrangling steps using dplyr pipes rather than base
* I created the [plots](http://rpubs.com/lgcarlson/trawledafigs) that Kathy and I discussed last week (biomass by latitude over decades, biomass weighted density by decade, and slope of center, leading, trailing edge)
* I used these plots to visualize what different proportions of biomass would look like as leading/trailing edges
* I read [Poloczanska et al. 2013](https://doi.org/10.1038/nclimate1958), [Hampe et al. 2005](https://doi.org/10.1111/j.1461-0248.2005.00739.x), [Knutsen et al. 2013](https://doi.org/10.1371/journal.pone.0067492), [Woolbright et al. 2014](http://dx.doi.org/10.1016/j.tree.2014.05.003), [Sunday et al. 2012](https://doi.org/10.1098/rspb.2010.1295), and [Haak et al. 2010](https://doi.org/10.1577/1548-8446-35.11.530). None had useful descriptions/definitions of leading/trailing edges

#### What did you struggle with?

* I struggled to find any description of how to define/calculate a leading/trailing edge. 
* I got stuck on the loop to assign monthly growth increment values. 

#### What would you like to work on next week?

* I will go back and try to finish the growth increment assignment loop. 
* I will continue to explore the leading/trailing edge literature to get a better understanding of how these are defined. 

#### Where do you need help from Kathy?

* It will be good to reconvene and discuss defining leading/trailing edges.   

#### Where do you need help from other lab members?

* We had further discussion about workflow/files organization in the shared Box folders. I'm still not sure how the trawl/Pew project fits in to everything, so I might need some help figuring out the best home for that work. 
------




### Date: 17 May 2019

#### Who did you help this week?

I found a conflict between the "here" and "lubridate" packages and posted the solution on the lab Slack page so other people can avoid it.

#### Who helped you this week?

Kathy and Tim helped me understand the salmon dataset better by taking some time to answer some of the big questions about it. Andrew suggested a Wednesday meeting, and we all brainstormed some good ideas to better integrate Box and a Git workflow, as well as longer-term goals and projects we want to work together on. 

#### What did you achieve?

* I wrote code to calculate monthly growth increments based on methods decribed by Todd et al. 2013 in a paper titled [A simple method of dating marine growth circuli on scales of wild one sea-winter and two-sea winter Atlantic salmon](https://www.nrcresearchpress.com/doi/10.1139/cjfas-2013-0359#.XN8CzchKi70).
* I created [glms](http://rpubs.com/lgcarlson/growthincrementglm) to better understand the effect of some of the cat vars on first year increments (age, state, season, etc).
* I compiled lists of missing data in Carlin dataset for Tim.
* I set up Git on a new computer and made it talk to R successfully!
* I wrote lots of loops, used some if/else statements, and improved my function writing/understanding substantially!

#### What did you struggle with?

* I struggled for a while on Friday to conceptualize a nested loop I thought I needed for the monthly growth calculation. I figured out the nested loop, but in the processed realized there was a much less verbose method. 

#### What would you like to work on next week?

* I will finish the monthly growth increment calculations.
* I will work on the trawl EDA Kathy and I discussed during our meeting on Friday.

#### Where do you need help from Kathy?

* I think we are all set for a while after our Friday meeting! 

#### Where do you need help from other lab members?

* I am looking forward to collaborating on our Shiny project. 
------




### Date: 10 May 2019

#### Who did you help this week?

I helped Andrew work through some Shared Box->RProject navigation using the 'here' package. He put together a cool "test run," then I worked through it on my computer to see if it would work as a shared code. I think we found and solved a few issues!

#### Who helped you this week?

Andrew, Miguel, Matt, and Kathy all helped me troubleshoot the memory limitation I ran into on my computer when running a shared code.

#### What did you achieve?

* I rewrote some of my hacky code using a more sophisticated loop
* I created a version-controlled R project and associated repository for the trawl data
* I worked on the [exploratory data analysis](http://rpubs.com/lgcarlson/CarlinEDA5102019) for the salmon growth data that Kathy and I talked about during this week's meeting
* I read a few papers about how to calculate leading/trailing edge
* I learned how to use the packages 'here' and 'formattable'

#### What did you struggle with?

* I struggled for quite some time with the memory problem on my computer before asking for help. Then, once I asked for help, a lot of time was spent by all parties trying to figure it out. I stopped working on the trawl data after Karen determined that we were sent the wrong computer. Hopefully that solves the problem, but it didn't make sense to keep spending time on fixing something that seems to work for everyone but me. 

#### What would you like to work on next week?

* I will keep working on the salmon growth data and figure out next steps for the analysis. 
* I did not get to it this week, so next week I would like to do some reading to figure out a better MS-CMR encounter history structure.

#### Where do you need help from Kathy?

* Meeting with Kathy and Matt at some point to get oriented to the trawl data would be helpful.
* There are still some unanswered questions about the salmon data that I have listed in the [Ask Kathy Freedcamp project](https://freedcamp.com/Lindsay_6rU/Ask_Kathy_pAt/todos). 

#### Where do you need help from other lab members?

* I don't necessarily need help from anyone, but I think I will do the function-writing Datacamp over the weekend or next week to improve my function skills. I wrote a few successful functions and loops this week, but I just couldn't figure out how to do one and reverted to the longhand approach. 
------



### Date: 03 May 2019

#### Who did you help this week?

This week, I spent a few hours working to learn more Git code on my own so I could be a more informed participant in the GitHub lab discussion on Wednesday. Though it didn't help anyone individually, I think active participation by everyone in the lab helps everyone else to learn too. 

#### Who helped you this week?

Miguel helped me by ammending his algorithm to work for my dataset. It is very well annotated and concisely coded, and I really appreciate him sharing his work so I didn't have to reinvent the wheel. 
Andrew helped the lab by creating slides and an exercise to help us further our GitHub discussion. He also did a really great job making this repository! 

#### What did you achieve?

* I wrote a loop to create a tagging history of all Carlin-tagged fish that can be merged with the recapture datasets
* I used the reshape packages to create encounter histories for recaptured salmon
* I integrated growth markers placed by Miguel's algorithm into the circuli dataset
* I did EDA on spatial and temporal trends in salmon growth data
* I made leaps and bounds in my understanding of Git!

> Awesome progress!

#### What did you struggle with?

* I struggled with figuring out how to code the multistate structure of the encounter histories. I used a pretty hacky approach that will probably work, but could be done better. 
* I struggled to figure out the organizaton of the trawl data.

> Join the club, it isn't the easiest. You may have already seen this, though just in case, the "SVDBS Elements by Table and Column" file on the shared NMFS Trawl Data folder is somewhat helpful. Definitely let me know if it would be easier to meet and discuss -- could loop in Andrew/Matt, too.

#### What would you like to work on next week?

* I would like to spend more time with the trawl data. 
* I would like to do some reading to figure out a better MS-CMR encounter history structure.

#### Where do you need help from Kathy?

* Meeting with Kathy and Matt to get oriented to the trawl data would be helpful.
* There are still some unanswered questions about the salmon data that I have listed in the [Ask Kathy Freedcamp project](https://freedcamp.com/Lindsay_6rU/Ask_Kathy_pAt/todos). 

> Awesome. I'll plan to connect with you and Matt on the trawl data and have a look at the FreedCamp questions!

#### Where do you need help from other lab members?

* I would like to continue to work collaboratively to all become proficient (enough) on GitHub.

#### Any other topics


