### 2019
* [10 May 2019](#date-10-May-2019)
* [17 May 2019](#date-17-May-2019)
* [24 May 2019](#date-24-May-2019)
* [31 May 2019](#date-31-May-2019)
* [7 June 2019](#date-7-June-2019)

# Weekly Notes
### Date: 7 June 2019

#### What did you achieve?

* I learned about CMIP5 models and all the complexity that surrounds them
* I read a lot on the best ways to create multimodel means and whether or not to use weighted model means 
* I downloaded and averaged 31 CMIP5 models and created both spatial and time series plots to be used with the shad project

#### What did you struggle with?

* I struggled with doing batch downloading of netcdf files from a NASA server. It is not a Thredds server and is password protected so it has some added complexity.
* I have downloaded some of the files individually but there are over 480 so individually is not the answer although works for the short term

#### What would you like to work on next week?

* I am going to continue figure out how to do a batch download. I am pretty much there but was jsut getting frustrated with minor errors so will tackel it again early next week

#### Where do you need help from Kathy?

At the moment I think I am good with what I have and will continue to chug along. I should have both RCP 4.5 and RCP 8.5 raster and timeseries files on hand as well as the NLDAS data on hand by the middle-end of next week

# Weekly Notes
### Date: 31 May 2019

### I forgot to write a post this week, so this is what I remember

* I learned about Shiny apps and how to code Shiny apps
* I coded a Shiny app to utilitze the Buoy Anomaly function. The app is available here https://mdzaugis.shinyapps.io/Anomaly_App/

# Weekly Notes
### Date: 24 May 2019

### I forgot to write a post this week, so this is what I remember

* I contributed to the review of a FO paper
* I read several other papers on lobster, specifically regarding degree days, and added to my annotated bibliography
* I re-wrote the UpdateBuoy functions to run a lot faster. It cut the runtime down from ~30 min to ~1 minute.
* I finished the Buoy Anomaly and stratification index function and incoorporated the new UpdateBuoy data format into those functions
* I need to remember to add a new function that puts the UpdateBuoy data back into its original (matrix style) format in case other people want to use the old functions


# Weekly Notes
### Date: 17 May 2019

#### What did you achieve?

* I finished the DataCamp on R markdown and several chapters of ggplot
* I started to make each r code page stand alone and incorporated the here package
* I read several papers on lobster and read the FO paper that we are reviewing a few times

#### What did you struggle with?

* I am trying to keep up with github and integrate it into my normal workflow

#### What would you like to work on next week?

* I am going to continue to read more about lobsters and do some exploratory data analysis on the phyiscal data in the GoMe

#### Where do you need help from Kathy?

At the moment I think I am good with what I have and will continue to chug along



# Weekly Notes
### Date: 10 May 2019

#### Who did you help this week?
I don't think I helped anyone

#### Who helped you this week?

Kathy during our meeting 
Kathy and Andy during the Lobster Collabrative meeting

#### What did you achieve?

* I incoorporated density into the update buoy function
* I succesfully ran and downloaded the OISST dataset and was able to create anomaly sst maps
* I finished writing a function to calculate and the temperature, salinity, or density anomalies for any buoy at any depth over several different time scales. 
* I also finished writing a function to calculate the stratification index anomalies.
* I incoorporated buoys N01 and M01 into the update buoys code

#### What did you struggle with?

* I struggled with adding N01 and M01 buoys to the code that downloads all of the buoy data at once. Those buoys have data for different depths than the other buoys and the current script doesn't allow variation in depth. I had to rewrite a buch of the code in order to add those buoys

#### What would you like to work on next week?

I am going to continue to work on the update buoy function to try and make it run a little faster. When I complete this I am going to combine the OISST and buoy data

#### Where do you need help from Kathy?

At the moment I think I am good with what I have and will continue to chug along

#### Where do you need help from other lab members?
Possibly when I start working up the OISST data - I'll give it some more work first
#### Any other topics

This space is yours to add to as needed.
