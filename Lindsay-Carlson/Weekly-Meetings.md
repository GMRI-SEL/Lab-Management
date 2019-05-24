### 2019
* [3 May 2019](#date-03-may-2019)
* [10 May 2019](#date-10-may-2019)
* [17 May 2019](#date-17-may-2019)
* [24 May 2019](#date-24-may-2019)

# Weekly Notes
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
* I read [Poloczanska et al. 2013](10.1038/nclimate1958), [Hampe et al. 2005](10.1111/j.1461-0248.2005.00739.x), [Knutsen et al. 2013](10.1371/journal.pone.0067492), [Woolbright et al. 2014](http://dx.doi.org/10.1016/j.tree.2014.05.003), [Sunday et al. 2012](10.1098/rspb.2010.1295), and [Haak et al. 2010](10.1577/1548-8446-35.11.530). None had useful descriptions/definitions of leading/trailing edges

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




### Date: 3 May 2019

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


