### 2019
* [26 July 2019](#date-26-july-2019)
* [19 July 2019](#date-19-july-2019)
* [12 July 2019](#date-12-july-2019)
* [28 June 2019](#date-28-june-2019)
* [29 April 2019](#date-29-april-2019)

# Weekly Notes
### Date: 19 July 2019

#### Who did you help this week?

* I helped Ally with her change point analyses by showing her how to change the parameters and penalty values for the type of algorithm used and sensitivity in detecting change points. I helped Lindsay in clarifying some of the data structure within the DFO data set.

#### Who helped you this week?

* Lindsay helped me with suggestions on looking at the correlations between the ERSST data and the calanus data. Andrew and Matt helped me by talking through modelling the salmon scale growth markers using SST and the calanus data using GAMs in a series of nested for loops.

#### What did you achieve?

* This week I was able to run some model variations using nested for loops to evaluate model performance across different spatio-temporal spaces and different growth mark increments.

#### What did you struggle with?

* I struggled with setting up the loops in a way to try out all the various combinations of SST and calanus data for different time periods and different migration areas.

#### What would you like to work on next week?

* Next week I would like to incorporate the 2014 2SW data into the analyses that Brandon sent on Thursday, put together a list of additional scales and go collect them, and look at the growth patterns between the hatchery and wild fish.

#### Where do you need help from Kathy?

* Taking a look at the GAM results and putting together a final list of additional scales to collect

#### Where do you need help from other lab members?

# Weekly Notes
### Date: 19 July 2019

#### Who did you help this week?

* This week the lab had some discussions with Andrew about order of operations when collapsing down daily spatial rasters into monthly means. I made a map of the Connecticut River watershed with the 3 temperature gage sites for the Shad project. I helped Lindsay with interpreting GAMs results

#### Who helped you this week?

* Andy was able to take a look at the spatial plots of the calanus predictions and confirm for me that the December results were off and should be replaced by interpolating November to January of the next year. Mike helped me with some reading materials explaining boosted regression trees.

#### What did you achieve?

* This week I worked on converting the calanus prediction results into a .grd file for fasting loading and subsetting. From there I was able to extract the monthly values of calanus abundance within each of the salmon migration area shapefiles. After that I averaged over all cells in each raster to get one monthly mean calanus abundance value for each migration area 1950-2018.

#### What did you struggle with?

* There were some strange results within the calanus predictions occurring at northern latitudes in the month of december. I was not sure whether these results were realistic or just a source of error from the model predictions.

#### What would you like to work on next week?

* Next week I would like to run GAMs using the salmon growth increments as the response variable, with SST and calanus abundance as the explanatory variables.

#### Where do you need help from Kathy?

* I would like to go over the model results with Kathy.

#### Where do you need help from other lab members?

* I could use help looking at the model results and evaluating model fits.

# Weekly Notes
### Date: 12 July 2019

#### Who did you help this week?

* This week I helped Ally by giving her some code for Tukey plots and I helped Andrew by making a merged shapefile for the DMR Lobster Management zones. I also talked with Mike and Lindsay about using dynamic time warping to cluster growth patterns...not sure if this method will be useful...to be determined!

#### Who helped you this week?

* This week Lindsay helped me with summarizing the months that smolts were released by year. Andrew helped me with setting Date attributes to raster files in order to query layers better.

#### What did you achieve?

* I presented some work to Tim and the salmon group, transferred scale samples to Tim, had productive discussions about the timing of annulus formation and possible misclassification of sea-age for PN data. I figured out how to produce Rmarkdown documents for the phenology work. I incorporated Brandon's new FMC locations and reanalyzed the data. I was able to figure out how to notate significance as a symbol overlay for the SST and growth marker spatial correlations.

#### What did you struggle with?

* I struggled with being able to calculate monthly means for each cell within a raster layer and then subtract those from corresponding months to create anomalies. After some discussion and some reading, I was able to figure it out. I had some trouble with selecting specific layers out of a raster stack but by the end of the week and talking with Andrew, we figured it out. I tried running GAMS on the SST and growth markers by year but I don't think there are enough data points (n=12) to use GAMs on the PN growth marker data.

#### What would you like to work on next week?

* I made some progress with subsetting the SST data from May to the following July rather than Jan to Dec and then performing the spatial correlations with the first year growth increments. The first three year-groups showed a clear positive correlation with SST but when the fourth year-group was included, things got messy. Strangely, on its own, the series of years from the fourth year-group correlated well with SST, just not when included with the rest of the years. I'd like to investigate this further and maybe try including the calanus abundance predictions as another variable in the linear regression.

#### Where do you need help from Kathy?

* It would be nice to discuss the more recent spatial correlation work with Kathy and show the changes between including the fourth year-group vs. not including and also talk about building-in the calanus abundance data into the model.

#### Where do you need help from other lab members?

I think talking with Lindsay and Mike about how we can integrate our datasets together for some analyses into the future might be productive.

#### Any other topics

This space is yours to add to as needed.
### Date: 28 June 2019

#### Who did you help this week?

* This week I helped Mike with his presentation by sending him some data summary slides for the Penobscot River Atlantic salmon growth data. I helped Lindsay with plotting salmon migration area shapefiles. I also helped Ally with plotting results from Tukey tests.

#### Who helped you this week?

* Lindsay helped me by discussing how we should work together to bring in SST data into our salmon scales growth marker analyses. Andrew helped me with some code for correlating SST rasters with salmon scale data. Kathy helped me by sending some tutorials on GAMs.

#### What did you achieve?

* This week I ran stat summaries for the salmon return time phenology data filtered by sea-age, put together sample size data tables for the growth data to make sure sampling distributions were good, starting looking into building GAMs for summer/winter metrics, and starting working on spatial correlations between SST and salmon scale growth marker data.

#### What did you struggle with?

* This week I struggled with reading up more on GAMs and trying to get an understanding of what is actually going on behind the scenes in order to build modles that are appropriate.

#### What would you like to work on next week?

* Next week I would like to continue working on the SST spatial correlations with the salmon scale growth marker data.

#### Where do you need help from Kathy?

* Next week I'll be heading to Orono to get more scale samples so I need Kathy to put together the list of scales that I'll collect

#### Where do you need help from other lab members?

#### Any other topics

This space is yours to add to as needed.

### Date: 29 April 2019

#### Who did you help this week?

Replace this text with a one/two sentence description of who you helped this week and how.

#### Who helped you this week?

Replace this text with a one/two sentence description of who helped you this week and how.

#### What did you achieve?

* Replace this text with a bullet point list of what you achieved this week.
* It's ok if your list is only one bullet point long!

#### What did you struggle with?

* Replace this text with a bullet point list of where you struggled this week.
* It's ok if your list is only one bullet point long!

#### What would you like to work on next week?

* Replace this text with a bullet point list of what you would like to work on next week.
* It's ok if your list is only one bullet point long!
* Try to estimate how long each task will take.

#### Where do you need help from Kathy?

* Replace this text with a bullet point list of what you need help from Kathy on.
* It's ok if your list is only one bullet point long!
* Try to estimate how long each task will take.

#### Where do you need help from other lab members?

#### Any other topics

This space is yours to add to as needed.
