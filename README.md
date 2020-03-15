# Apple Watch Data Exploration (WIP)

I got an Apple Watch last year (as a birthday gift to myself). As a data enthusiastic, I am always eager to learn more about myself with data. Now I have the chance. I exported the data from my Apple Watch, which generated a 250MB XML file, and decided to play with it a little bit.

## About The Dataset

The 'export.xml' file unzipped from the Apple Watch export has two parts:  
1. **Records Data**  
This includes all your health records (all the ['HKQuantityTypeIdentifier' objects](https://developer.apple.com/documentation/healthkit/hkquantitytypeidentifier)) like energy burned, heart rate, stand time, body mass, etcs. -- basically those you will see in your 'Health' APP.  
2. **Workout Data**
This includes all the workout records (all the ['HKWorkoutActivityType' objects](https://developer.apple.com/documentation/healthkit/hkworkoutactivitytype) from the 'Activity' APP， like the type, duration, distance, and energy burned.  
3. **Daily Summary Data**  
This includes a daily stats summary from the 'Activity' App, basically your move/exercise/stand hour target vs. actual.  

Of course the dataset will not be posted in this repo due to data privacy, but you can always find a snapshot in the code :)  

## Notebooks (WIP)
1. [**Apple Watch Export Data Extraction**](https://github.com/yudong-94/Apple-Watch-Data-Exploration/blob/master/Apple%20Watch%20Export%20Data%20Extract.ipynb)  
This notebook is on how to extract the data from the exported XML file and convert to pandas dataframes and csv files.   
2. [**Heart Rate Data EDA**](https://github.com/yudong-94/Apple-Watch-Data-Exploration/blob/master/Apple%20Watch%20Export%20Data%20-%20Heart%20Rate%20EDA.ipynb)  
This notebook focus on understanding, analyzing, and visualizing the heart rate data extrated. It looked at the relationship and difference among heart rate, resting heart rate, and walking heart rate records, and explored the pattern of the heart rates during weekdays/weekends and on different hours of a day.  
2. [**Energy Data EDA**](https://github.com/yudong-94/Apple-Watch-Data-Exploration/blob/master/Apple%20Watch%20Export%20Data%20-%20Energy%20Data%20EDA.ipynb)  
This notebook focus on understanding, analyzing, and visualizing the energy burned data extrated. It tried to understand the granularity of each record, looked at the difference beetween Basal Energy Burned and Active Energy Burned, explored their trend over time, and pattern on different time of day and on different weekdays.    

## Open Questions

Below is a list of questions I am interested to look at:  
1. What is my typical heart rate looks like, how it is distributed, and how it differs while resting / walking / workout?  
2. How is my energy burned elevating (my daily move target has increased multiple times since I've been doing routine workout now)? Relationship between heart rate and energy burned?  
3. How different my life pattern is during weekday vs. weekends from the perspective of these health metrics?  
4. How is my workout records trending? Given the same workout form every day (well, Ring Fit Adventure on Switch for me in the past three months), am I playing longer? Am I getting used to it looking at the hear rate and energy burned during the workout?  
