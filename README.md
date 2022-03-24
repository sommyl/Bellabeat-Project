# Sophie_Portfolio
Data Analytics Portfolio

# [Project 2: Bellabeat: Project Overview](https://github.com/sommyl/Sophie-Portfolio/blob/main/Cyclistic%20Project.md) 
* Bellabeat is a high-tech wearable fitness smart device manufacturer focused on women.
* The business task is to obtain insights on trends of smart device usage for marketing strategy of product growth.

## Code Used
**SQL Github:** https://github.com/sommyl/Bellabeat-Project/blob/main/Bellabeat%20SQL%20Code.sql

**Tableau:** https://public.tableau.com/app/profile/sophie.liu3966/viz/Bellabeat_16470858013980/Story1

## Data Cleaning

The dataset is made up of personal tracker activity from thirty-three fitbit devices for 3 month period from 12 March 2016 to 12 May 2016 which contains the key information as below

* Device ID
* Activity Date/timestamp
* Exercise intensity level split by minutes and distance (very active/moderately active/light active/sedentary)
* Step count
* Calorie count
* Total metabolic equivalents
* Total sleep time
* Total time in bed

Following changes were made in the cleaning process

*	Deleted columns "tracker distance" and "logged activity distance" considered duplicate information to column "total distance"
*	Summed up total minutes recorded each day to check against a 24 hour day for completeness
*	Distinct count of device ID for worksheets containing sleep info (24), daily exercise info (33) and heart rate info (14)
*	Joined 3 tables to combine hourly calories, intensities and steps in one table on ID and activity hour (CTE function)
*	Joined 3 tables to combine sleep, mets and exercise in one table with use (CTE function)
*	Created day of the week based on activity date
*	Created 2 categories of users with active users being defined as having on average 1 hour very active and fairly active exercise per day (case function)

## EDA & Visualisation 
* The users have not worn or used the device all day at all times as shown in total hours tracked less than 24 hours.
* Considerable gap exists between active users and less active users measured by average activity level per day.
* Exercise activity picks up during 12pm-2pm and 5pm-7pm with active users engaging in more intensive exercise resulting in more calorie burn.
* There is slight variance of amount of exercies throughout the week with highest step count and calorie burn being recorded on the weekends.
* Time in bed and time asleep is positively correlated. Active users spending less time in bed to get the same amount of sleep time. This could be due to the reason that more exercise help people sleep better or active users spend less sedentary time in bed, which is inclusive. 
* Heartrate data has not been incorporated in the analysis due to small sample being collected.

![alt text](https://github.com/sommyl/Bellabeat-Project/blob/main/Hours%20tracked.png "Hours Tracked")
![alt text](https://github.com/sommyl/Bellabeat-Project/blob/main/Avg%20Activity%20Level%20by%20user%20status.png "Avg Activity Level by User Status")
![alt text](https://github.com/sommyl/Bellabeat-Project/blob/main/Avg%20activity%20level%20by%20hour.png "Avg Activity Level by Hour")
![alt text](https://github.com/sommyl/Bellabeat-Project/blob/main/Activity%20level%20by%20day%20of%20the%20week.png "Avg Activity Level by Day pf the Week")
![alt text](https://github.com/sommyl/Bellabeat-Project/blob/main/Sleep%20time%20vs%20time%20in%20bed.png "Relationship between sleep time and time in bed")

## Recommendation
The selling point of Bellabeat is help users improve wellbeing and develop healthy habit by engaging in appropriate level of exercise and having sufficient good quality sleep.

Following recommendation is based on insights from the dataset:-
* **Lacking of exercise or low level of exercise** seem to be prevalent amongst majority of users (27 users have less than 1 hour moderate to intensive exercise daily out of 33 devices being studied). Use of Bellbeat smart device serves as a reminder and incentive to keep up with fitness goals. 
* Bellabeat should encourage device wear more frequently as data tracking shows **not all 24 hour** are tracked at all times. It is also recommended that an interactive report be provided to users with live syncing to monitor user activity against benchmark set by medical professionals to encourage users to be more active.
* The popular time for exercise is **between 12pm-2pm and 5pm and 7pm** and users exercise more **on the weekends** than weekdays. Bellabeat could set up notifications in the identified time blocks to remind people to exercise.
* Due to **the positive correlation between time in bed and sleep time**, Bellabeat could send reminders for people to go to bed at the recommended sleep hour by medical professionals.
