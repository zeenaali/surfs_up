# surfs_up
a SQLIte weather analysis

## Project Overview

## **Purpose**

To open a Surf’n’Shake shop, a shop that sells surf boards and ice cream in Oahu, Hawaii, the weather has to be in our favor most days of a year. A perfect spot for the shop is a place with the right balance of warm temperatures, sunny days throughout the year and just enough rain to keep the vegetation green. If those criteria are met, we can be confident that new shop will rise and shine. To ensure that we will choose the right spot, I want to make some data-driven decisions; therefore, this analysis focuses on the temperature and rainfall for the past 7 years from 2010 to 2017, specifically for June and December, the two months that are apart enough to ensure that we have a good condition year-round. In order to have enough data, I am analyzing data from six weather stations in Oahu, Hawaii. The analysis consists of two parts:

- Temperature analysis for June and December from 2010 to 2017.
- Rainfall analysis for June and December from 2010 to 2017.

## **Background**

This shop can easily become a popular spot, potentially expanding to other Hawaiian Islands and other further-distance islands. Because of the potential quick turn-around, the analysis is built by using quick and fast tools:

• SQLite a popular database engine, a version of SQL, that is stored locally and supports quick testing and easy prototyping.

• SQLAlchemy a query tool design for SQLite to query SQLite databases.

## **Resources**

Data Source:

- hawaii.sqlite

Environment:

- Python 3.7

Software:

- Jupyter Notebook
- SQLite

## **Results**

The analysis focuses on the temperature and rainfall from six different weather stations on Oahu, Hawaii from 2010 to 2017 for June and December specifically.

### Comparison of the Temperatures for June and December
1. Number of data

- There are less data for December (1517 data points) than for June (1700 data points).

2. Dispersion of the data

- Temperatures are more spread out in December (std = 3.7) than in June (std = 3.3).
-  June’s mean and median are 74.94 °F and 75.00 °F respectively.
- December’s mean and median are 71.04 °F and 71.0 °F respectively.
- Maximum temperature in December is 83 °F and in June 85 °F.
- Minimum temperature in December is 56 °F and in June 64 °F.

3. Quartiles

- 1st quartile: 25% of all data is below 69 °F in December and 73 °F in June.
- 3rd quartile 75% of all data is below 74 °F in December and 77 °F in June.

![image](https://user-images.githubusercontent.com/99419112/164543863-89ddcece-d21e-439e-85dc-cb94a2201c5f.png) ![image](https://user-images.githubusercontent.com/99419112/164543892-072f7f80-3729-41e8-8114-8578f4f95517.png)

 Measures of Central Tendency of Temperatures for December and June in Oahu, Hawaii.
                       
### Comparison of the Rainfall for June and December

1. Number of data

- There are less data for December (1405 data points) than for June (1574 data points).

2. Dispersion of the data

- Rainfall quantity is more spread out in December (std = 0.5) than in June (std = 0.33).
- June’s mean and median are 0.13 inches and 0.02 inches respectively.
- December’s mean and median are 0.21 inches and 0.03 inches respectively.
- Maximum rainfall in December is 6.42 inches and 4.43 inches in June.
- Minimum rainfall in December is 0 inches and 0 inches in June.

3. Quartiles

- 1st quartile: 25% of all data is at 0 inches in December and 0 inches in June.
- rd quartile 75% of all data is below 0.15 inches in December and 0.12 inches in June.

![image](https://user-images.githubusercontent.com/99419112/164544163-04efec35-94f3-4670-a0e2-2f67023c6457.png) ![image](https://user-images.githubusercontent.com/99419112/164544193-fa1c70dc-4bb4-449d-afd7-74aa3b9a1fc6.png)

  Measures of Central Tendency of Rainfall for December and June in Oahu, Hawaii.

## Summary

Descriptive statistics from the queries above provide quick results and tells us a lot about the weather in that area. However, to fully understand the weather trend, I have provided additional analysis and explanation.

### Temperatures for June and December

From the temperature report we can see that there is not much difference in the weather in June and December, indicating mild and steady temperatures year-round. Mean and median – also known as 2nd quartile - are closely together, meaning that distribution of the data is not spread out. To find out protentional outliers and other trends the box and whiskers chart can tell us more about that.

![image](https://user-images.githubusercontent.com/99419112/164544342-d8a52cc8-8dc5-4cbf-adfc-2f2d777cb985.png)

Box and Whiskers Plot of Temperatures for December and June in Oahu, Hawaii.

From the graph we can see that there are just a few outliers. There are more outliers below the lower boundary in December, however the minimum temperature is 56 °F.

### Rainfall for June and December

The first difference that we notice is the max rainfall in June and December (4.43 and 6.42 inches respectively) and in both cases, highly above the mean. Also, standard deviation is high, mean and median or 2nd quartile are far apart, meaning that distribution of the data is highly spread out. That indicates the presence of extreme values in the dataset. The easiest way to determine outliers is to plot box and whiskers chart.

![image](https://user-images.githubusercontent.com/99419112/164544491-7d3119e5-2fe3-430b-8606-5a170fbd181e.png)

Box and Whiskers Plot of Rainfall for December and June in Oahu, Hawaii.

From the chart we can see that there are quite a few outliers, to be exact 183 in June and 205 in December (calculations). Those outliers have enough power to impact the mean, yet 183 and 205 data points out of 1574 and 1405 respectively is not that much. That indicates isolated extreme rainfall. This analysis capture weather data for 7 years from 2010 to 2017. To see the difference year to year I provided another graph of average rainfall grouped by year.

![image](https://user-images.githubusercontent.com/99419112/164544593-2abdf7e3-351d-43bd-bf54-a97de289210d.png)

                Average Rainfall for December and June per year in Oahu, Hawaii.

From the graph above we can see there was a lot of rainfall in December 2010 with significant drop in the following years. The rainfall became pretty steady in the following years with simiral quantaties in both months.




