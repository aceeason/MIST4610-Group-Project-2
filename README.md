# MIST4610-Group-Project-2
Group 2

## Members:
1. Sean Donovan - [@sean4565](https://github.com/sean4565)
2. Aaron Eason - [@aceeason](https://github.com/aceeason)
3. Gilbert Fahnbulleh - [@gsf11597](https://github.com/gsf11597)
4. Navi Khan - [@NaviKhan15](https://github.com/NaviKhan15)
5. Kiera Lumley - [@ksl05149](https://github.com/ksl05149)
8. Steven Thomas - [@st11521](https://github.com/st11521)

## Dataset Description:
Our group selected the NWS_WEATHER_ALERT_EVENTS because we wanted to analyze weather alert patterns, and gain a better understanding of weather alerts, reaction, and types that happened across the country. Our dataset has 18 columns and 2.8 million rows. 
The provider of this data is the National Weather Service and is found through SNOWFLAKE_PUBLIC_DATA_FREE.PUBLIC_DATA_FREE.NWS_WEATHER_ALERT_EVENTS. 

Key Columns:
- EVENT_TYPE (VARCHAR)
- EVENT_SEVERITY (VARCHAR)
- SENTTIMPSTAMP (TIMESTAMP_NTZ)
- COUNTY_GEO_ID (VARCHAR)

## Questions and Justification:
Question 1: What is the average lead time (time from when the alert is sent and when the event actually begins) to prepare for Extreme vs. Severe events, and which specific event type provides the shortest window for public response? The relevant columns are EVENT_TYPE, EVENT_SEVERITY, SENT_TIMESTAMP, and ONSET_TIMESTAMP. This question requires calculating interval gaps between two times. It also requires aggregation and filtering to exclude post-onset alerts (where the event has already started) to ensure the average isn't skewed by ongoing or past warnings. This reveals the technical limitations of the forecasting. If extreme tornado warnings have a significantly shorter lead time than severe ones, it highlights a critical vulnerability in emergency preparedness where the most dangerous events are the hardest to predict in advance.

Question 2: Which event types spike in which months? 
The relevant columns are EVENT_TYPE, SENT_TIMESTAMP, ONSET_TIMESTAMP. This questions requires calculating which type of event occurs during what time in the year it is. It requires aggregation and filtering to coordinate month, and weather occurence type. 

## Data Manipulation:


## Analysis and Results:
![Question 1 Queries](question1dash.png)
Query 1: The chart shows the average number of minutes between an alert and when the event actually starts. It reveals that high velocity events such as tornadoes have significantly smaller preparation times compared to slower events like winter storms. It also highlights where it is more difficult to forecast events, as those with shorter intervals have much slimmer margins for error.

Query 2: This heatgrid categorizes extreme events into specific lead-time buckets to visualize the actual window of opportunity the public has to seek safety. By identifying what percentage of the most dangerous events provide less than five minutes of warning, you can pinpoint specific event types where current forecasting technology fails to provide a safe margin of error. The data further proves that tornado watches are the most common critical events, and extreme cold watches give people much more time to prepare.

## Streamlit App
