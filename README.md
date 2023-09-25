# Project_1
Bootcamp: Project 1
# Car Accidents data Analysis
## Uk Government Data 2005-2015
## Data Set Found at:
### Severity Classification: https://www.gov.uk/government/publications/guide-to-severity-adjustments-for-reported-road-casualty-statistics/guide-to-severity-adjustments-for-reported-road-casualties-great-britain

### Original data: https://www.data.gov.uk/dataset/c0eec478-ef19-4234-826f-8efb9563eda2/road-safety

# Team Members
1. Jo Alvo
2. Habib Rehman
3. Tamunosaki Owukio Miller Amachree
4. Maliha Mukhtar
5. Chin Kelly

# Project Description/Outline
Road safety is critical concern for many countries, where road crash fatalities and disabilities is being considered as a major public health concern. In this project we will be doing **Exploratory Data Analysis**  on U.K. Traffic Accident Data (10+years) from 2005 to 2015 to Analyse real-world problem of road accidents based on **Accident Severity levels depending on Road Types, Light conditions, Journey Purposes, distribution of Accidents based on Male/Female Drivers, Vehicle Types**... 

# Research Question
To better guide the analysis we formed the following questions related to Road Safety and Traffic Accidents:
What is the severity of accidents over the last decade?
When do accidents usually happen related to Road Types?
What is the distribution of accidents and their severity levels depending on Light conditions?
what sex of drivers are invoved in most of the accidents?
What is the age distribution of drivers involved in the accidents?
What type of Vehicles are involved in most of the accidents?


# Libraries:
* Python
* Pandas  (Data Processing, and manipulatoin)
* NumPy   (Data Processing, and manipulatoin)
* Matplotlib (Data Visualization)

# Data Loading and Cleaning:
 UK Car Accidents Data is comprised of three CSV files: 'Accidents0515.csv' , 'Casualties0515.csv', 'Vehicles0515.csv'. After merging these three files using (Pd.merge), we filter data by local authority set to Birmingham, Coventry, Dudley, Sandwell, Solihull, Walsall and Wolverhampton only. Then we dropped any rows with NaN/empty/missing values.Afterwards we Create a clean DataFrame by dropping the duplicate rows by its Accident Index. Finally we saved our Cleaned Data as a new csv file to perform all of our analysis.

# Data Analysis
## Distribution of Accidents depending on their severity levels from 2005 to 2010
As our data is mainly categorical and in the data set it is in the form of categories. There is a seperate CSV file that provides all the encoding for the categories.
We performed  Exploratory Data Analysis on ** Uk Car Accident Data **  set  using Pandas functionalitis . First  we Filtered the data based on the severity levels:
 * Fatal 
 * Serious
 * Slight

 By using the GroupBy Function we checked the number of accidents in a 10 years time span. By making the use of  conditionals we dropped our analysis to 5 years time span to check is there any change in the distribution of Severity levels in this time period (2010 to 2014). 
We used  MatplotLib to visualise the data and make several pie charts, bar graphs, box plots to show the distribution of accidents by their Severity levels.

## Accident Severity levels by Road Types
 * Roundabouts
 * Single _Carriageways
 * Dual_Carriageways
 * Oneway_Street
 * Slip Road
It is observed through extensive Data Analysis and Visualisation through bar graphs that most fatal , severe and slight accidents happened on Single carriage ways. It is obvious that these roads shows the most peril for the drivers and cause more accidents than any other type of roads.  
 
 ## Assessment of Casualty Numbers versus Time of Day
we have filtered the data by combining accidents that have occurred during specific times of day into intervals, such that we can better assess when accidents are most likely to occur. 
We have a pie chart showing that majority of accidents over the time period assessed, in the West Midlands, occur during afternoon hours of 12:00 - 17:59. Common knowledge tells us that this is usually the time of day when road users use their vehicles for school runs, and the evening commute home after work. Although we cannot infer whether these accidents are occurring specifically during the school run or the commute home, we can definitely recommend that further care should be taken when driving during these hours.

## Analysing The Light Conditions and their Impact on the Severity Levels
In the government data file, the road safety key has defined values in column **'Light_Conditions'** with the below keys-

    1 : Daylight
    4 : Darkness - lights lit
    5 : Darkness - lights unlit
    6 : Darkness - no lighting
    7 : Darkness - lighting unknown
    -1 : Data missing or out of range
    We are going to combine the data under key 5 and 6, as both involve the roads being unlit. We dropped the data points from key 7 and -1 as this could potentially skew or create bias in our data because we do not know if the roads were lit or not. By analysing the data we Came to know that most of the accidents happened during Day light. do diagnose it further we analyse teh Journey purpose of the people and concluded that the reason behind can be the travel to work and school drop off and pick up journeys.
## Analysing Accidents by Drivers Age and Sex

By analysing the Age of Drivers we came to know that Fatal accidents are most common in Male drives and the most common age group is from 26 to 35. This shows us that in our data we have a trend and this can be used to predict insurance premiums for certain groups. 

## Analysis oF vehicle type and severity of Accidents
The type of vehicle involved in an accident does impact the severity of the accident, we could see in both our bar chat and pie chat that there was a 
noticeable difference in accident severity based on the type of vehicle involved, and also number of vehicles involved also plays  a role in accident severity. Multiple-
vehicle collisions were more likely to result in high-severity accidents compared to single-vehicle incidents.

## References-
Guide used to combine date and time: https://stackoverflow.com/questions/17978092/combine-date-and-time-columns-using-pandas
Guide used to create time bins: https://www.appsloveworld.com/pandas/100/10/how-to-bin-time-in-a-pandas-dataframe?expand_article=1
Stack OverflowStack Overflow
Combine Date and Time columns using pandas
I have a pandas dataframe with the following columns:
data = {'Date': ['01-06-2013', '02-06-2013', '02-06-2013', '02-06-2013', '02-06-2013', '03-06-2013', '03-06-2013', '03-06-2013', '03-06-2013', ...
Hire Developers, Free Coding Resources for the DeveloperHire Developers, Free Coding Resources for the Developer
[Code]-How to bin time in a pandas dataframe-pandas
Coding example for the question How to bin time in a pandas dataframe-pandas
 
https://www.gov.uk/government/publications/guide-to-severity-adjustments-for-reported-road-casualty-statistics/guide-to-severity-adjustments-for-reported-road-casualties-great-britain
https://www.data.gov.uk/dataset/c0eec478-ef19-4234-826f-8efb9563eda2/road-safety






