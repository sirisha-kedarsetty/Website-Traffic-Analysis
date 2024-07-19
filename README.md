# Website-Traffic-Analysis


## Table of Contents

   - [Project Overview](#project-overview)
   - [Data Source](#data-source)
   - [Tools utilized](#tools-utilized)
   - [Data Cleaning steps](#data-cleaning-steps)
   - [Key Metrics](#Key Metrics)
   - [DAX codes used for analysis](#dax-codes-used-for-analysis)
   - [Results](#results)
  

### Project Overview
Analyze website traffic data across various traffic sources, device categories, browsers, content segments, and geographic locations. Additionally,
incorporate traffic trends observed over different time intervals.


### Data Source
The primary dataset used for this analysis is an excel format dataset cantaining detailed information about page views, traffic sources ets.

### Tools Utilized

- Cleansing the data : Microsoft Excel and Power query editor.
     - [Download](https://microsoft.com)
- Visualization and Analysis : Power BI

### Data Cleaning steps

In the intial data prepation phase, I performed the following tasks:
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
        
     -Average_Session_Duration = AVERAGEX(Website_Traffic_Data,Website_Traffic_Data[Session_Duration_Seconds]/3600)
     -Bounce_Rate =   Var Bounced_Session = Calculate([total_Number of Sessions],Website_Traffic_Data[Page_Views_Per_Session]<2)
                                            RETURN
                                              Divide(Bounced_Session,[total_Number of Sessions])
   
     -Total_Number of Sessions = COUNT(Website_Traffic_Data[Session_Id])
     -Total_Page_Views = Sum(Website_Traffic_Data[Page_Views_Per_Session])
     -Total_session_Duration_Hours = SumX(Website_Traffic_Data,Website_Traffic_Data[Session_Duration_Seconds]/3600)

  ### Results

    The dashboard offers a comprehensive 360-degree view of total website session duration , Bounce Rate etc. , including 
    insights into how sessions , bounce rate are varying for different dimensions such as device types , content types & different
    cities.


   ### Output

![Webtrafficanalysis](https://github.com/user-attachments/assets/343996bf-34d6-4e6a-9b80-b7d95f7ad7ff)

![Webtraffic2](https://github.com/user-attachments/assets/da61eacc-bb2b-4512-9008-662c29317a26)
