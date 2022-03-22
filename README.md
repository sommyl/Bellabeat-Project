# Sophie_Portfolio
Data Analytics Portfolio

# [Project 2: Bellabeat: Project Overview](https://github.com/sommyl/Sophie-Portfolio/blob/main/Cyclistic%20Project.md) 
* Bellabeat is a high-tech fitness smart device manufacturer focused on women.
* The business task is to obtain insights on trends of smart device usage for marketing strategy.

## Code Used
**SQL Github:** https://github.com/sommyl/Sophie-Portfolio/blob/main/Cyclistic.sql

**Tableau:** https://public.tableau.com/app/profile/sophie.liu3966/viz/Cyclistic_16450573041030/Story1

## Data Cleaning

The dataset contains personal tracker activity from thirty fitbit users for period from 03.12.2016-05.12.2016. The analysis is focused on the daily records log for exercise and sleep with following key information:-

* User ID
* Activity Date/timestamp
* Level of exercise intensity by minute (very active/moderately active/light active/sedentary)
* Step count
* Calory count
* Total sleep time
* Total time in bed
* Total mets

Following changes were made in the cleaning process

*	Created a new table and used union all function to merge 12 CSV files of monthly ride information with in total c. 5 million rows 
*	Created a new column for ride length as duration from start time to end time by using DATEDIFF fuction
*	Created a new column for day of the week from start date by utilising DATENAME function to convert YYYYMMDD HH:MM:SS date format into day of the week  
*	Shortened ride ID to save memory as this information is not critical
*	Removed columns "End date and time" and "Station ID" as this information is redundant 
*	Removed 2,207,583 rows for ride length less than 10 minutes as this is considered too short for trip length
*	Removed 4,754 rows with nil latittude and longtitude due to incomplete information for geographic mapping

## EDA & Visualisation 
Analysis is focused on observing difference in ride patterns between casual and member riders in order to derive insights for conversion strategy. All information given in the dataset has been utilised to construct analysis as follows
* Number of rides and ride length (derived from rider ID and time information) have been compared between casuals and members by frequency of month, day of the week and time of the day in order to identify the optimum period for advertising with widest reach 
* Only 24 users have recorded their sleep out of 33 users who recorded their daily exercise level.

![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/month.png "Number of Trips and Trip Length by Month")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/weekday.png "Number of Trips and Trip Length by Day of the Week")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/hour.png "Number of Trips and Trip Length by Hour")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/map.png "Map of Start and End Location")

## Recommendation
In order to achieve maximum reach of casual riders, it is recommended that 
* Advertisement is to be placed **during summer season** **on the weekend** **from 12pm to 5pm** as data indicated that this is when casual riders are most active measured by average number of trips taken.
* The ideal location for advertising is **in Harbour and Millennium Park area** which captures higher density of start and end point for casual riders.
* Based on ride length comparison which shows casuals takes longer rides in kms than members, the company could some form of communication as prompt at the end of each ride to recognise a milestone of kms achieved in comparison to an average member user to incentivise future rides which may subsequently result in member conversion.
