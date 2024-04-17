# DATA SCIENTIST TECHNICAL TEST
*Guidelines*

## Instructions
- This test includes 4 tasks, it is advised to carefully read the instructions for each task.
- Any suitable method can be used, and there are no restrictions on online resources or packages. 
- The objective of the test is to see your own work: the main criteria for evaluation may not be the answer per se but how you manage to obtain this answer. 
- It is important to provide a commented code that can be read by anyone.
- Results should be provided as a R or Python script. You can also provide a Rmarkdown or Jupyter notebook. 

## Problematic
In order to take decisions on the management of a coastal reservoir, we need to be able to anticipate the variations of sea level in the next 30 minutes. Sea level is mainly determined by tides.
The objective of this assignment is to provide a module that forecasts the observed sea level for the next 30 minutes.

## Datasets
You will be asked to use 2 datasets for this test:
- astronomical_tide.csv (astronomical tide for August 2017),
- observed_sealevel.csv (observed sea level for August 2017).

All datasets are available here: [https://github.com/Karim-Claudio/suez-datascience-test](https://github.com/Karim-Claudio/suez-datascience-test)
 
## Tasks
Note that the analysis should be carried out using Singapore Time (SGT = UTC+8).

### Task 1 - Astronomical tide
1. Read the file astronomical_tide.csv: this file contains 2 columns, the time, and the tide value. Time is expressed in UTC. 
2. Plot the astronomical tide according to time.

### Task 2 - Observed sea level
1. Read the file observed_sealevel.csv: this file contains 2 columns, the time (already expressed in SGT) and the sea level value.
2. Plot the observed sea level according to time. 
3. Identify if the dataset presents any outliers and correct the data if necessary.

### Task 3 - Joining the datasets
The observed sea level is available every 30 minutes, whereas the astronomical tide is available every minute. 
1. Down-sample the astronomical tide dataset, the frequency of the new dataset should be aligned with the main objective.
2. Join the observed sea level and the astronomical tide down sampled.
3. Is the observed sea level correlated to the astronomical? What is the method you used?

### Task 4 - Forecast
The objective of this section is to build a module to forecast the sea level:
1. Build a training dataset using data until 2017-08-30 23:30:00 (included).
- The unknow variable should be the sea level for a specific timestamp.
- The explanatory variables should include past values for the sea level, past value for the astronomical tide and its real value for the timestamp you want to predict.
2. Design a forecast model and predict the value of the sea level for 2017-08-31 00:00:00 SGT.
- What model did you apply and why?
- What kind of metric can you use to assess the accuracy of your forecast?
3.	Using the same model, forecast the observed sea level for all timestamps from 2017-08-31 00:30:00 SGT until the end of the timeline.
- It should be assumed that starting 2017-08-31 00:00:00 (included), the value of the sea level is unknown.
- What kind of metrics can you use to assess the goodness of fit of your model over this longer period?
