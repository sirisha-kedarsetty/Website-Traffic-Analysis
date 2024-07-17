# Website-Traffic-Analysis


## Table of Contents

   - [Project Overview](#project-overview)
   - [Data Source](#data-source)
   - [Tools utilized](#tools-utilized)
   - [Data Cleaning steps](#data-cleaning-steps)
   - [Exploratory Data Analysis(EDA)](#exploratory-data-analysis(eda))
   - [DAX codes used for analysis](#dax-codes-used-for-analysis)
   - [Results and findings](#results-and-findings)
   - [Recommendition](#recommendition)

### Project Overview
Analyze website traffic data across various traffic sources, device categories, browsers, content segments, and geographic locations. Additionally,
incorporate traffic trends observed over different time intervals.


### Data Source
HR Data: The primary dataset usedd for this analysis is an excel format dataset cantaining detailed information about employees and wages.

### Tools Utilized

- Cleansing the data : Microsoft Excel and Power query editor.
     - [Download](https://microsoft.com)
- Visualization and Analysis : Power BI

### Data Cleaning steps

In th intial data prepation phase, I performed the following tasks:
     1. Data Loading and inspection
     2. Handling the missing values
     3. Data cleansing and formating
     4. Merging different tables and prepared Master table. 

### Key Metrics

Website_Traffic_by_Device_Sources


     1.Session Duration & Page Views - DeviceType
     2.Bounce Rate by Content Segment 
     3.Session Duration and Page Views- Traffic Source
     4.Bounce Rate by Device Type
     5.Bounce Rate by Website Traffic Source
     6.Bounce Rate by Different Browser

Website_Traffic_Trend_over_Time

     1.Total Session Duration(Hrs) - Trend for Device Types
     2.Total Session Duration (Hrs) - Trend for Website
     3.Traffic Source Average Session Duration (Hrs) - Overall
     4.Trend Bounce Rate - Monthly Trend
     5.Bounce Rate - Daily Trend

Geography_based_Website_Traffic

     1.Total Page Views - Regionwise
     2.Total Session Duration - Regionwise
     3.Bounce Rate - Regionwise
     4.Total Number of Sessions - Top 5 Cities
     5.Total Session Duration - Top 5 Cities
     6.Total Page Views -Top 5 Cities
     7.Bounce Rate - Top 5 Cities
         
  ### DAX codes used for analysis
        
       - Average salary = Average(data[Salary]) 
       - Avg.Leavebalance = Average(data[Leave Balance])
       - Cumulatuve Count = VAR Currentdate =LASTDATE(data[Date of Join])
                   Return
                   Calculate([Head Count],all(data[Date of Join]),data[Date of Join] <= Currentdate)
       - Head Count = count(data[Emp ID])
       - LBL over 20days = Calculate([Head Count],data[Leave Balance] >20
       - Max_Salary = Max(data[Salary])
       - Min_Salary = Min(data[Salary])


  ### Results and findings:

       1. Increase in recruitment over time.
       2. Product Manager Job title has the highest salary
       3. Maximum nuber of employees are in mid 30years

   ### Output
![Screenshot 2024-07-17 105642](https://github.com/user-attachments/assets/0e6ae838-d4fd-4d3b-85be-ffa8e262627e)


     


  ### Recommendition:

    Based on the analysis I recomend the following actions:

       1. Pay grade of packing associate should be increaseed.
       2. There are 29 employees with LBL over 20 days need to be given time for vacation so that there is work life balance.
       3. Number of female employees need to be increaseed.
