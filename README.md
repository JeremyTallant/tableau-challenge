# Citi Bike Analysis
![image](https://user-images.githubusercontent.com/112406455/217119594-e9639cc0-082c-491a-acf7-4b2f3a750550.png)
## Background 
Congratulations on your new job! As the new lead analyst for the [New York Citi Bike](https://en.wikipedia.org/wiki/Citi_Bike) program, you are now responsible for overseeing the largest bike-sharing program in the United States. In your new role, you will be expected to generate regular reports for city officials looking to publicize and improve the city program.

Since 2013, the Citi Bike program has implemented a robust infrastructure for collecting data on the program's utilization. Each month, bike data is collected, organized, and made public on the [Citi Bike Data](https://citibikenyc.com/system-data) webpage.

However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have questions about the program, so your first task on the job is to build a set of data reports to provide the answers.
## Deployment
Here is the link to the Tableau dashboard: https://public.tableau.com/app/profile/jeremy.tallant/viz/citibike_16762569400730/Story1
## Instructions
Your task in this assignment is to aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena.

1. Design 2–5 visualizations for each discovered phenomenon (4–10 total). You may work with a timespan of your choosing. Optionally, you can also merge multiple datasets from different periods.

2. Use your visualizations (not necessarily all of them) to design a dashboard for each phenomenon. The dashboards should be accompanied by an analysis explaining why the phenomenon may be occurring.

3. Create one of the following visualizations for city officials:

    * **Basic**: A static map that plots all bike stations with a visual indication of the most popular locations to start and end a journey, with zip code data overlaid on top.

    * **Advanced**: A dynamic map that shows how each station's popularity changes over time (by month and year). Again, with zip code data overlaid on the map.

    * The map you choose should also be accompanied by a write-up describing any trends that were noticed during your analysis.

4. Create your final presentation:

    * Create a Tableau story that brings together the visualizations, requested maps, and dashboards.

    * Ensure your presentation is professional, logical, and visually appealing.
    
## Data Source
1. The first step of the process was gathering all the monthly csv files (January 2018 - December 2020) from the [Citi Bike Data](https://citibikenyc.com/system-data) webpage and storing them in a folder called "data".
2. Then I created a Jupyter Notebook file called "[citibike.ipynb](https://github.com/JeremyTallant/tableau-challenge/blob/main/citibike.ipynb)" to clean and merge all the monthly csv files into one csv file to load into Tableau.
3. Here is the step by step process of the data cleansing:
   * First import pandas.
   <img width="1084" alt="Screenshot 2023-02-13 at 4 46 14 PM" src="https://user-images.githubusercontent.com/112406455/218593152-ef1d9f47-2703-4376-b778-635b99482c6f.png">
   
   * Read in all csv files for a single year in a pandas dataframe, store in a list, and then concatenate into a single dataframe.
   <img width="1215" alt="Screenshot 2023-02-13 at 4 46 27 PM" src="https://user-images.githubusercontent.com/112406455/218593900-1df2f2c1-927b-4650-abd3-517e8054c5f9.png">
   
   * Repeat the step for the remaining years.
   <img width="1215" alt="Screenshot 2023-02-13 at 4 46 35 PM" src="https://user-images.githubusercontent.com/112406455/218594370-6c34b4b1-e184-434d-a8af-b0717afd70ca.png">
   <img width="1214" alt="Screenshot 2023-02-13 at 4 46 43 PM" src="https://user-images.githubusercontent.com/112406455/218594455-7beeab76-a39d-4349-92a5-043a16a05235.png">
   
   * Combine all three dataframes into a single dataframe.
   <img width="1212" alt="Screenshot 2023-02-13 at 4 46 58 PM" src="https://user-images.githubusercontent.com/112406455/218594806-4331abbd-8cc4-49c1-8bfc-fd6b105899eb.png">
   
   * Change the values in the gender column from the numerical value to the actual value.
   <img width="1214" alt="Screenshot 2023-02-13 at 4 47 07 PM" src="https://user-images.githubusercontent.com/112406455/218595129-b560a3d6-92a1-48fd-b9bd-e8cb1d643ae1.png">
   
   * Then save the dataframe to a csv file.
   <img width="1212" alt="Screenshot 2023-02-13 at 4 47 14 PM" src="https://user-images.githubusercontent.com/112406455/218595280-98ac8c4d-2ebb-4a97-a187-dd6978def8f7.png">
   
   **Please note that the large size of the CSV files precludes their storage in this repository and in GitHub's Large File Storage. As a result, the CSV files have been added to a .gitignore file.**
## Dashboards
A homepage and three dashboards were made from the citibike data.
### Homepage
* The homepage gives a brief overview of the project and gives a quick description of the contents of each dashboard.
<img width="1426" alt="Screenshot 2023-02-13 at 5 31 51 PM" src="https://user-images.githubusercontent.com/112406455/218598439-9bccde87-fcf3-4da7-9fe3-80d229359f45.png">

### User Analysis 
* This dashboard analyzes trips based on user type, gender, and age. It also contains an analysis of trips based on hours and weekdays and total number of trips per month.
<img width="1426" alt="Screenshot 2023-02-13 at 5 32 45 PM" src="https://user-images.githubusercontent.com/112406455/218599192-abf1dfc0-9a14-4d48-8a7a-683cdbf34528.png">

### Station Analysis
* This dashboard analyzes trips based on stations. It also contains comparisons between weekdays and weekends and then average trip duration of each month.
<img width="1425" alt="Screenshot 2023-02-13 at 5 33 02 PM" src="https://user-images.githubusercontent.com/112406455/218600480-f7e3f38e-2424-4950-b594-a03e5ae015c4.png">

### Geographic Analysis
* This dashboard contains two maps and the location of the start and end station. The size and color of the marker indicates the total number of trips that started or ended at each station.
<img width="1425" alt="Screenshot 2023-02-13 at 5 33 31 PM" src="https://user-images.githubusercontent.com/112406455/218600539-d287fd71-6f8b-4e2d-805a-e60477abd38b.png">

**A user-friendly interface has been created utilizing Tableau dashboards, allowing for seamless navigation between pages. Please access the link in the deployment section to explore the interactive dashboard and gain valuable insights.**

## Summary
<img width="986" alt="Screenshot 2023-02-13 at 6 17 04 PM" src="https://user-images.githubusercontent.com/112406455/218605560-74bbe56a-b822-4b78-b39e-956f143bfffa.png">

* An evaluation of the data covering the time period from 2018 to 2020 shows a total of 1,095,641 trips made using bicycles in New York City. This represents a decrease of 4.83% over the three-year period. The observed decline in trips can be attributed to the adverse effects of the COVID-19 pandemic, including the associated shutdowns, on the usage of bicycles.
* A comparison of the data from 2018 to 2020 reveals a decrease of 30.20% in the number of subscribers, while there was a simultaneous increase of 374.90% in the number of customers. This disparity in trends can be attributed to the impact of the COVID-19 pandemic on the usage of bicycles in New York City.
* Over the specified time period, there appears to be a positive trend in the number of female riders, with an increase of 12.55%, while the number of male riders has decreased by 22.29%. While the reason for this trend is not definitively known, it could potentially be attributed to improved safety and security measures for female riders. Further analysis would be required to establish this hypothesis.

<img width="822" alt="Screenshot 2023-02-13 at 6 46 50 PM" src="https://user-images.githubusercontent.com/112406455/218609202-043e2682-5796-42c4-91c1-5bdad3f347ad.png">

* It is noteworthy that the peak utilization of citibikes in New York City occurs during the weekday, specifically during the hours of 8 a.m. and 5 p.m., as a significant number of commuters utilize bicycles for their daily commute.

<img width="589" alt="Screenshot 2023-02-13 at 6 56 45 PM" src="https://user-images.githubusercontent.com/112406455/218610532-c600a3e0-0abc-431d-bb29-5a2d90f447e7.png">

* An examination of the data reveals that the pattern of peak bicycle usage in New York City remained consistent during 2018 and 2019, with the busiest periods occurring during the weekdays. However, in 2020, a notable deviation from this trend emerged, with weekends experiencing the highest levels of bicycle usage. This shift can likely be attributed to the widespread adoption of remote work as a result of the COVID-19 pandemic. 

<img width="621" alt="Screenshot 2023-02-13 at 7 05 26 PM" src="https://user-images.githubusercontent.com/112406455/218611841-d35104a1-4fe0-4b5b-9669-f3fc596f4eb4.png">

* A review of the data by month reveals that the highest usage of bicycles in New York City occurs during the summer months of July, August, and September, in comparison to the winter months. In April of 2020, a marked decrease in bicycle usage was observed, which can be attributed to the restrictions imposed during the early stages of the COVID-19 pandemic.

<img width="602" alt="Screenshot 2023-02-13 at 7 05 30 PM" src="https://user-images.githubusercontent.com/112406455/218612417-bc985457-005a-453f-a641-3425d3a01e91.png">

* The analysis of the data indicates that the majority of bicycle riders in New York City belong to the age group of 29 to 43, with a prevalence of male riders among this demographic.

<img width="1163" alt="Screenshot 2023-02-13 at 7 19 08 PM" src="https://user-images.githubusercontent.com/112406455/218614331-c7e16678-be24-4ba5-a91e-700b3da6248a.png">

* An examination of the data reveals a disparity in the number of start stations compared to the number of end stations.

<img width="812" alt="Screenshot 2023-02-13 at 7 19 16 PM" src="https://user-images.githubusercontent.com/112406455/218614627-d3fa0863-5a3d-4b8b-ad3b-6ccdf6c28036.png">

* The analysis of the data, as depicted in the chart, indicates that Grove St PATH and Hamilton Park are the most frequently used stations for both starting and ending trips.

<img width="615" alt="Screenshot 2023-02-13 at 7 19 20 PM" src="https://user-images.githubusercontent.com/112406455/218615289-c4ec6639-0ecd-4d15-9ada-11ac052315d8.png">

* An examination of the graph presenting the average trip duration, measured in minutes, per month reveals a noteworthy increase in 2020 compared to the average trip durations in 2018 and 2019. This deviation can be attributed to the closure of businesses and an increased amount of time spent outdoors, particularly during the summer months, as a result of the COVID-19 pandemic. 

   







