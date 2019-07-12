### 2019

* [5 July 2019](#date-5-July-2019)
* [28 June 2019](#date-28-June-2019)
* [21 June 2019](#date-21-June-2019)
* [14 June 2019](#date-14-June-2019)
* [7 June 2019](#date-7-June-2019)
* [10 May 2019](#date-10-May-2019)
* [17 May 2019](#date-17-May-2019)
* [24 May 2019](#date-24-May-2019)
* [31 May 2019](#date-31-May-2019)

# Weekly Notes
### Date: 5 July 2019
* I made a rmarkdown that compares gam and lm for the river temperature data and air temperature
* Created a comprehensive markdown that compares all sites and projections
* Wrote up the methods for analysing the CMIP5 data, air temp observations, and river temp data

### Who helped you this week?
* Mike and Andrew heled me with some gam modeling of the CT river temperature

### Who did you help this week?
* I helped Allie with the buoy data to create anomalies and stratificaiton
* I explained my methods of using python and wget to download LOCA data

# Weekly Notes
### Date: 28 June 2019

Short week, I took vacation on Monday 24/6

### What did you achieve?

* I worked on temperature projections and bias corrections
* I came up with three functions to add in the data analysis
  + climatology function
  + Function to calculate the difference in observed vs. projected data
  + Funciton to correct for any biases in the projected data


# Weekly Notes
### Date: 21 June 2019

Short week, I took vacation on Tuesday and Friday.

### What did you achieve?

* I worked on the temperature projections and added Turner Falls to the observation and projection data. 
* Created some markdown documents to give an overview of the different projections
* Compared observed and modeled air temperature data at the Middle Haddam site to see if a bias correction is necessary

# Weekly Notes
### Date: 14 June 2019

#### What did you achieve?

* I figured out how to use the function wget in terminal to recursively download all of the pw protected links in a text file and combine the individual netcdf files into a single file in r
  + This worked great for the 480 monthly averaged netcdf files but will not work for the 354,000+ hourly values
* With help from Alex, I was able to use a Python script to subset and download data from a DAP server that was pw protected 
  + There does look to be a way to do this from R but I had issues using the rJava funcitons 
* I requested the RCP4.5 and RCP8.5 LOCA data for both min and max temperature and received those datafiles
  + wrote a R code to get the 32 model mean and combine min and max into a daily average
* I have compiled all of the data in R scripts 
  + Middle Haddam RCP 4.5 model mean
  + Middle Haddam RCP 8.5 model mean
  + Thomsonville RCP 4.5 model mean
  + Thompsonville RCP 8.5 model mean
  + Middle Haddam NLDAS observation - daily means
  + Thompsonville NLDAS observations - daily means
  + Middle Haddam and Thompsonville gage river temp observations

#### What did you struggle with?

* It took awhile to come up with a method to subset and download the data that didn't take 60 hours. Even though the files were only 80kb there were so many it took forever

#### What would you like to work on next week?

* I am going to continue with the shad project
  + create a daily average from the hourly observational data
  + create a daily mean projection from the min temp and max temp LOCA projections
  + compare LOCA with observation
  + compare LOCA and observation with the river gage data


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
