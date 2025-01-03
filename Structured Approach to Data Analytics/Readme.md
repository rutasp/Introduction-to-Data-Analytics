# Structured Approach to Data Analytics Project

# Steps to stress balance

## ASK 

#### Problem: 
Manage stress levels by understanding how my daily step count correlates with stress levels.

#### Problem I want to solve:

•	reduce stress levels

•	consistently achieve targeted step count (current target 5000/day)

#### Key questions: 

•	What would motivate me to make more steps in a day?

•	How steps influence stress levels?

•	Are there any patterns in more stressful days/hours?

•	What changes in daily routine can help improve stress resilience?

#### What would qualify as a successful result: 

Regularly achieve a set daily step goal

Observe a consistent decrease in stress levels on days with higher step counts.

#### Determining solution:

•	Regularly achieve a set daily step goal.

•	Decrease in stress levels on days with higher step counts.

•	Develop strategies to maintain a balanced and active lifestyle.

## PREPARE

#### Needed data:

•	Hourly/daily steps data

•	Hourly/daily stress data

#### Used data source: Mi Fitness smart band data

## PROCESS

•	Data download from Mi Fitness app. Storing it on local drive.

•	Cleaning of the selected data. Downloaded data had more that 1,048,576 rows in Excel, but for the sake of this project I needed just a tiny bit of it. 

•	Raw data looked like this:

<img width="514" alt="image" src="https://github.com/user-attachments/assets/3ac32527-05c0-4101-8458-c6e2d092e639" />

•	Found identifier file with explanations:

<img width="354" alt="image" src="https://github.com/user-attachments/assets/b562d7f7-97cf-43fd-9656-e8e3d118f843" />
 
•	Figuring out how to translate given number (time column) to an actual date and time (Unix Timestamp)

<img width="380" alt="image" src="https://github.com/user-attachments/assets/16449157-f7c3-47b1-856d-8c01aee5bff9" />

•	Cleaning and sorting of the data (“text to columns”, filtering, creating Pivot tables for hourly and daily data aggregation, changing formats of different data types).

After all these steps data was complete, correct, and relevant for the project. As well aggregated and summarized in appropriate manner. Maximum observations in the task – 200, so in order to see some patterns I’ve used 2 weeks of data for steps (206 data points) and stress analysis (153 data points).

## ANALYZE

During this stage I’ve noticed that stress data was recorded just during periods of sleep. I found in the app definition what is stress analysis: “evaluation of stress level is based on heart-rate variability (HRV), the time between heartbeats. HRV increases during relaxing activities and decreases during stress. Device measures stress level when you’re inactive and might get blank areas, representing time periods unable to determine stress due to too many actions”. This means that lower stress score number actually indicates more stress.

High level data revealed that highest stress levels (lowest points of blue line in the chart below) were on the same days with lowest steps and could see some correlation between data. After the lowest point (22nd of Jan), on most stressful day in the analysis daily movement helped gradually stabilise stress levels in the upcoming days. Of course, correlation doesn’t mean causation, but it could be one of the factors influencing positive impact on stress levels. Most resilient to stress days were 16th and 21st of January, when daily steps averaged around 4165.

<img width="455" alt="image" src="https://github.com/user-attachments/assets/ffb21f90-a107-41d8-85bd-e448d19fd5f9" />

Heatmap of hourly data of stress (below) shows how stress levels continuously increases in mornings (represented by orange-red cells) and usually reduces in evenings around 9-11PM (green-yellow). 
Interestingly, some data was collected during the day as well (as by definition above usually stress is recorded just during inactive hours). I’ve noticed spikes during the end of the working day as represented by orange and red cells (corresponding to 28th of January and 22nd of January). 												
														
![image](https://github.com/user-attachments/assets/a60e3c1b-19c1-4f61-ac89-3a945595e24f)
											
In conclusion, the analysis reveals that physical activity influences my stress levels. Knowing that during those days when steps decreased significantly from the day before stress simultaneously increased shows negative relation between these two factors.
To mitigate stress, I should consistently achieve my daily step goal, for e.g. take regular breaks to walk around during working day, consider going to the office more often and walk little distances instead of using car. While there are various factors influencing stress levels, such as sleep quality and balanced nutrition, taking some action is better than doing nothing.

