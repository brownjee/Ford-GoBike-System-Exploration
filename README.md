# Ford GoBike System Exploration

## Dataset

The dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. It has 183412 rows and 16 columns. Some wrangling process was needed to tidy the dataset for exploration. After tidying the dataset, I was left with 174952 rows and 19 columns which is saved as a new dataframe called `goBike_clean` (This dataset is what I used for the analysis). it has variables (columns) like `start_time`, `duration_sec` , `user_type`, `member_gender`, member_birth_year etc.
Key things to note after tidying the data that `start_time` now becomes three columns namely `start_time(hr)`, `start_day` and `start_month`. Then start_time column is dropped (This is seen in `goBike_clean` dataframe, the dataset used for analysis)
The main data set can be downloaded [here](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv)


## Summary of Findings

For the exploration, I started by looking at the distribution of the main features of interest start_time(hr), start_day, start_month, duration_sec, and user_type. I also looked at member_gender, and age. It was obsereved that:

#### For Univariate Exploration:

 - Most of the trip were made between the hours of 7, 8, 9 and 16, 17, 18 hour, with the highest hours being 17 followered by 8. There are also some riders between the early hour of 0 to 4 am. Also, there are some riders within the hour of 22 and 23
 - Most of the ride where made on weekdays with Thursday being the most frequent day followered by Tuesday. Also people rarely go on ride during the weekends as Saturday and Sunday has the lowest number of riders.
 - The whole dataset is only for the month of Febuary so no need to futher investegate this variable
 - Most of the trip took around 300 - 900 seconds duration, with a high peak at 500 sec.
 - About 150000+ are subscribers and Customers are below 20000

#### For Bivariate Exploration In this section, here are the questions asked and the observations

##### On which day(s) and at what time were most trip taken?
 - Thursdays has the highest trip made at the 17 hour compared to the rest of the days followed by Wednesday. Also, Friday has the highest trip at the 8 hour compared to the rest of the days. Although, the relationship between Friday and Tuesday for the 8 hour are closely related, as well as Thursday and Wednesday for the 17 hour.

##### How long does the average trip take and on which day?
- The longest trips happens on weekends, Saturdays and Sundays. It took about 800 to 850 seconds on average.

##### Which user took the longest trip on average
 - customers spent more time on average compare to subscribers.
 - The longest trip for a subscriber takes about 600 seconds
 - The longest trip for a customers takes about 1400 seconds

##### How old is the rider that took the longest trip on average
the rider that took the longest trip is 18 with about 2400 seconds on average. Followed by 78 and 141.
The distribution of the riders age and the time the took seems to really correlate and start falling for some older ages.
From 19 years to 66 years are riding between 600 - 800 seconds
The older age from 67 to 119 seems to have inconsistent number of seconds.

#### For Multivariate Exploration

The longest trip was taken by a customer at the hour of 3 for about 5000 seconds. The gender type "Other" took the longest trip at the hour of 3 for about 4200 seconds followed by the "Male" gender for about 2500 seconds. Customers takes more long trip than subscribers The females actually takes longer trip than males Most Riders tends to go on trip at the early hours of 0, 2 and 3

In summary, from the analysis, I discovered that although weekends had the lowest number of trip across the dataset, The longest trips happened on weekends, Saturdays and Sundays. It took about 800 to 850 seconds on average.

## Key Insights for Presentation

For the explanatory analysis/presentation, I polished and visualized some of the analysis done in the exploratory analysis section which are:
 - How long does the average trip take and on which day?
 - On which day(s) and at what time were most trip taken?
 - Which user took the longest trip on average and at what time of the day
Although these questions already have plots made, for the presentation, the plots needed to be polished by adding the axis labels, title and removing some unwanted marks that may confuse the viewers.
