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
2. Then I created a Jupyter Notebook file called "citibike.ipynb" to clean and merge all the monthly csv files into one csv file to load into Tableau.
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
   
   







