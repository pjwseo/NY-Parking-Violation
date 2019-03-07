# Understanding Parking Violation of New York in 2018
## By Paul Seo

### Purpose:
This project is the first public dataset on Kaggle that I chose to work with. I wanted a learning experience through assess and wrangling this dataset programmatically and representing the data with inline visualizations. I will be coming back to this project to include further visualizations using tableau.

### Dataset:
This dataset provided by the City of New York is available on Kaggle (https://www.kaggle.com/new-york-city/ny-parking-violations-issued). It contains 5.9 million parking violations and 43 columns.

This dataset is by far the messiest I have had to work with. After selecting 8 columns I wanted to work with, I took a close look at each of the columns with how I will be using them later in mind. First I combined date and time information into a python datetime object, removing any invalid time data from the dataset. then I made a list of all vehicle registration states and removed all other vehicles as realistically speaking, a vehicle in NY is most likely registered from within North America (US, Canada, Mexico). For vehicle body types, make, and color I looked through the most common values, fixed typos and made a list to filter ones I will be using for analysis. Finally, I categorized each of the parking violations into seasons and time of day using the datetime information. After this wrangling process, the dataset contains 3.5 million parking violations and 9 columns.

### Summary of Findings:
Virtually all vehicles that violated NY parking law in 2018 were registered in NY. 

This parking violation data contained violations that had nothing to do with parking. Hence I removed all violations that had nothing to do with parking (Ex. Driving through red light, driving over speed limit, etc.). 

The Top 10 most common parking violations were found and categorized into 5 unique violations - they were responsible for approximately 82% of all parking violations in NY. 

When looking at the vehicle body types of vehicled found to be violating parking laws in NY, I got what looks to be a representation of the whole vehicle population in NY where SUV were the most common vehicle body type. 

Looking at the distribution of vehicle manufacturers of vehicles that violated NY parking law in 2018, I found that the Top 5 most common vehicle manufacturers made up more than 50% of all vehicles found in the dataset. 

Vehicle colors of vehicles found to be violating parking laws in NY in 2018 was dominated by monochrome colors, White, Gray, and Black combined for approximately 89% of all vehicles in the dataset.

As expected, vehicle years were distribution was left skewed where there were more newer cars in the dataset. I caught a very interesting pattern when looking at the distribution around 2007 - 2009. I could spot where The Great Recession in the US could have possibly made impact that would be visible here in the NY parking violation dataset where the number of 2008 and 2009 year vehicles dip in count.

When looking at parking violation by season, it was no surprise that more violations were filed when the weather is nice, specifically during Summer and Fall. Parking violations during NY's Summer and Fall in 2018 were responsible for 87% of all violations. I found that only 295 parking violations were recorded during Spring months, which seem impossible. For now, I conclude that this is due to human error and this dataset may not be complete. It is not impossible that my data wrangling somehow removed Spring parking violations specifically, but I will come back to this later.

Parking violations recorded during morning and afternoon made up 82% of all parking violations. This is not surprising because many of us take the car out and are out and about during these periods of time.

### Conclusion:
Through this analysis I was able to confirm common conceptions regarding city parking violations, such as when most parking violations occur, which violations are most common, and what color of cars. As I was not provided with the data of the whole vehicle population of NY, I was not able to build a prediction model for what kind of cars are likely to cause a parking violation. However, I have gained a tremendous amount of experience in working with large datasets (This one has more than 5 million rows) and programmatically assessing and wrangling data.

I promise to come back to this dataset to visualize further insights with tableau!
