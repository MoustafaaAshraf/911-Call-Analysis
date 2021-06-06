# Analytical Study of 911 Calls

![alt text](a.jpg "911")

In this study, using a dataset acquired from Kaggle, an analytical study of behaviours and patterns of emergencies reproted to 911 is performed.

**Please find report at: https://mosafehashf.medium.com/data-analysis-911-calls-db6d80f90d78**

<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Objectives" data-toc-modified-id="Objectives-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Objectives</a></span></li><li><span><a href="#Gathering-data-:-The-database-breakdown" data-toc-modified-id="Gathering-data-:-The-database-breakdown-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Gathering data : The database breakdown</a></span></li><li><span><a href="#Assessing-Data-/-Exploratory-Data-Analysis" data-toc-modified-id="Assessing-Data-/-Exploratory-Data-Analysis-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Assessing Data / Exploratory Data Analysis</a></span></li><li><span><a href="#Data-Preparation" data-toc-modified-id="Data-Preparation-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Data Preparation</a></span><ul class="toc-item"><li><span><a href="#Reason-for-Call-(-Emergency-Type-)" data-toc-modified-id="Reason-for-Call-(-Emergency-Type-)-4.1"><span class="toc-item-num">4.1&nbsp;&nbsp;</span>Reason-for-Call ( Emergency Type )</a></span></li><li><span><a href="#Acquiring-Data-time-objects" data-toc-modified-id="Acquiring-Data-time-objects-4.2"><span class="toc-item-num">4.2&nbsp;&nbsp;</span>Acquiring Data-time objects</a></span></li></ul></li><li><span><a href="#Analysis" data-toc-modified-id="Analysis-5"><span class="toc-item-num">5&nbsp;&nbsp;</span>Analysis</a></span></li><li><span><a href="#Discussion-and-findings" data-toc-modified-id="Discussion-and-findings-6"><span class="toc-item-num">6&nbsp;&nbsp;</span>Discussion and findings</a></span></li></ul></div>




## Objectives

The study aims to answer four questions:

    1. What is the most common Reason for a 911 call?
    
    2. What are the most emergency-charged months of the year?
    
    3. What are the most hours of the day of reporting EMS?
    
    4. What are the most days of the week of reporting EMS?
    
    5. Busiest traffic day in the week?
    
    

## Gathering data : The database breakdown

The database is a record of all records the emergency 911 calls over an interval of time. each call is recorded as an instance while recording features of each call. The features are broken down as follows:

These two features represent the location as identified by the Opearator

    1. lat : String variable, Latitude

    2. lng: String variable, Longitude

    3. desc: String variable, Description of the Emergency Call, reason and nature of emergency

    4. zip: String variable, Zipcode of the reporter as provided by the caller

    5. title: String variable, Title

    6. timeStamp: String variable, YYYY-MM-DD HH:MM:SS

    7. twp: String variable, Township

    8. addr: String variable, Address

    9. e: String variable, Dummy variable (always 1)

## Assessing Data / Exploratory Data Analysis

In this section various questions about the data is answered:

    1. Which features are available in the dataset?

    2. How many rows and columns does the dataset have?

    3. Which features are categorical?

    4. Which features are numerical?

    5. Which features contain blank, null or empty values?

    6. What are the data types for various features?
    
    
## Data Preparation

### Reason-for-Call ( Emergency Type )

It is not effective to study the pattern of reason-for-call from the title provided, as the title feature include not only the emergency type, but also a description of the specific emergency.

### Acquiring Data-time objects

The date and time for each emergency call is recorded as a timestamp object. The time stamp object would'nt be helpfull as is. Hence it is converted to Month, Hour for later analysis.

we can turn the timestamp from a string into a timestamp object for more reliable view overwriting the 'timestamp' feature applying the apply method using the pd.date_time method that changes A time stamp feature of a type string into an actual timestamp object.

To study patterns of 911 calls with relation to months, days-of-week ,and hours, new columns needs to be created breaking down the time stamp into an acumlation of months, days-of-week, or hours along the whole period.


## Analysis

Please see within the notebook provided.

## Discussion and findings

1. Most of the calls are for the reason of EMS followed by Traffic.

2. January and December are the most emergency charged months of the year. Moreover, the reason for call is mainly EMS and Traffic Emergencies.

3. The reporting of EMS across the hours of the day mainly spikes during working hours.

4. Friday is the most day of the week with calls reporting EMS and Traffic Emergencies.

5. The late hours of the night has the least emergency calls However on the weekends, there is a more emergency calls after midnight.