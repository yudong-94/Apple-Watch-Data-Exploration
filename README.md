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

### Open Questions

Below is a list of questions I am interested to look at:  
1. What is my typical heart rate looks like, how it is distributed, and how it differs while resting / walking / workout?  
2. How is my energy burned elevating (my daily move target has increased multiple times since I've been doing routine workout now)? Relationship between heart rate and energy burned?  
3. How different my life pattern is during weekday vs. weekends from the perspective of these health metrics?  
4. How is my workout records trending? Given the same workout form every day (well, Ring Fit Adventure on Switch for me in the past three months), am I playing longer? Am I getting used to it looking at the hear rate and energy burned during the workout?  
