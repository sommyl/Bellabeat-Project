# Sophie_Portfolio
Data Analytics Portfolio

# [Project 2: Bellabeat: Project Overview](https://github.com/sommyl/Sophie-Portfolio/blob/main/Cyclistic%20Project.md) 
* Bellabeat is a high-tech wearable fitness smart device manufacturer focused on women.
* The business task is to obtain insights on trends of smart device usage for marketing strategy.

## Code Used
**SQL Github:** https://github.com/sommyl/Bellabeat-Project/blob/main/Bellabeat%20SQL%20Code.sql

**Tableau:** https://public.tableau.com/app/profile/sophie.liu3966/viz/Cyclistic_16450573041030/Story1

## Data Cleaning

The dataset contains personal tracker activity from thirty-three fitbit devices for 3 months period from 12.3.2016-12.5.2016. The activity log records following key information

* Device ID
* Activity Date/timestamp
* Exercise intensity level split by minutes and distance (very active/moderately active/light active/sedentary)
* Step count
* Calory count
* Total metabolic equivalents
* Total sleep time
* Total time in bed

Following changes were made in the cleaning process

*	Deleted columns "tracker distance" and "logged activity distance" which is duplicate information of another column
*	Summed up total minutes recorded each day to check total minutes being recorded against a 24 hour day for completeness
*	Distinct count of device ID reveals total sleep records of 24 vs total exercise records of 33
*	Joined 3 tables to combine hourly calories, intensities and steps in one table on ID and activity hour with use of CTE
*	Joined 3 tables to combine sleep, mets and exercise in one table with use of CTE
*	Created day of the week based on activity date
*	Created 2 categories of users with active users being defined as having on average 1 hour very active and faily active exercise per day with use of case function
* Heartrate data has not been incorporated in analysis due to only 14 devices' data being captured.

## EDA & Visualisation 
* Considerale gap exists between active users and inactive users measured by average exercise per day.
* The device has not been worn or put in function all day at all times as shown in total hours tracked.
* Exercise picks up during 12pm-2pm and 5pm-7pm with active users engaging in more intensive exercise resulting in more calory burn.
* There is slight variance of amount of exercies throughout the week with highest step count and calory burn being recorded on the weekends.
* Time in bed and time asleep is positively correlated. Active users spending less time in bed to get the same amount of time asleep. This could be due to more exercise help people sleep better or active people spending less sedentary time in bed, which is inclusive. 

![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/month.png "Number of Trips and Trip Length by Month")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/weekday.png "Number of Trips and Trip Length by Day of the Week")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/hour.png "Number of Trips and Trip Length by Hour")
![alt text](https://github.com/sommyl/Sophie-Portfolio/blob/main/map.png "Map of Start and End Location")

## Recommendation
The selling point of Bellabeat is help users improve wellbeing and develop healthy habit by engaging in appropriate level of exercise and having sufficient good quality sleep.

Following recommendation is based on insights from the dataset:-
* Lacking of exercise or low level of exercise seem to be prevalent amongst majority of users - 27 users have less than 1 hour moderate to intensive exercise daily out of 33 devices being studied. Use of Bellbeat smart device serves as a reminder and incentive to keep up with fitness goals. Bellabeat should encourage device wear more frequently as data tracking shows not all 24 hour are tracked at all times. It is also recommended that an interactive report be provided to users with live syncing to monitor user activity against benchmark set by medical professionals to encourage users to be more active.
* The popular time for exercise is after lunch and after work and on the weekends. Bellabeat could set up notifications in the timeblock to remind people to exercise.
* Due to the positive correlation between time in bed and sleep time, Bellabeat could send reminders for people to go to bed at the recommended sleep hour by medical professionals.
