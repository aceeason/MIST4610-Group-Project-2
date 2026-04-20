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

## Questions and Justification:
Question 1: What is the average lead time (time from when the alert is sent and when the event actually begins) to prepare for Extreme vs. Severe events, and which specific event type provides the shortest window for public response? The relevant columns are EVENT_TYPE, EVENT_SEVERITY, SENT_TIMESTAMP, and ONSET_TIMESTAMP. This question requires calculating interval gaps between two times. It also requires aggregation and filtering to exclude post-onset alerts (where the event has already started) to ensure the average isn't skewed by ongoing or past warnings. This reveals the technical limitations of the forecasting. If extreme tornado warnings have a significantly shorter lead time than severe ones, it highlights a critical vulnerability in emergency preparedness where the most dangerous events are the hardest to predict in advance.

## Data Manipulation:


## Analysis and Results:


## Streamlit App
