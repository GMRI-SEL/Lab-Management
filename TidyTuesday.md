## Welcome to Tidy Tuesday!
### Overview
The [Tidy Tuesday](https://github.com/rfordatascience/tidytuesday) project is an effort kickstarted by the R for Data Science Community (R4DS) that provides weekly datasets for researchers to use to enhance their coding skills and build collaborations. Dr. Mills' Integrated Systems Ecology Lab participates in Tidy Tuesdays, along with other interested folks in the GMRI Research Department, *every Thursday afternoon.* As the founders describe, "the intent of Tidy Tuesday is to provide a safe and supportive forum for individuals to practice their wrangling and data visualization skills independent of drawing conclusions" [Tidy Tuesday official GitHub repository](https://github.com/rfordatascience/tidytuesday). Whether you consider yourself an expert in data manipulation and vizualization using the Tidyverse language, or if you've never seen the "%>%" operator before, all are welcome and encouraged to participate!

### Getting started
Before doing anything, double check that you have a recent version of R and RStudio installed. Now, once you've done that there are two ways to get going. 

*Option One -- Reading in data using the https links*
1. On the [Tidy Tuesday repository page](https://github.com/rfordatascience/tidytuesday) scroll down to the "DataSets" section and then find the data set for that week, which is usually always going to be the last entry/most recent dataset. 
2. Click on the link for the data (third column) and this will bring you to a new webpage. 
3. Copy the code chuck right below "Get the data!". For example, the ramen ratings dataset would be *ramen_ratings <- readr::read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2019/2019-06-04/ramen_ratings.csv")*
4. Open up R Studio and a new script. At the top of your script (and after installing the tidyverse package) type
```{r}
library(tidyverse)
ramen_ratings <- readr::read_csv("https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2019/2019-06-04/ramen_ratings.csv")
```
5. Off you go! 

*Option Two -- Fork/clone and establish upstream connection to the Tidy Tuesday repository*
This is a bit more involved. However, it will likely make things a bit easier/more reproducible. Additionally, it will help increase our Git/GitHub skills and who doesn't want to do that?!
