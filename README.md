# EXP-2--Implementation-of-time-series-analysis-and-decomposition
## AIM:
Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.
## ALGORITHM:
## STEP 1: 
Import the required packages like pandas and numpy
## STEP 2: 
Read the data using the pandas
## STEP 3: 
Perform the decomposition process for the required data.
## STEP 4: 
Plot the data according to need, either seasonal_decomposition or trend plot.
## STEP 5: 
Display the overall results.
## PROGRAM:
## DEVELOPED BY:P SYAM TEJ
## REF NO: 212221240056
```
import pandas as pd
import numpy as np
from statsmodels.tsa.seasonal import seasonal_decompose
df=pd.read_csv('AirPassengers.csv')
df.head()
df.set_index('Month',inplace=True)
df.index=pd.to_datetime(df.index)
df.dropna(inplace=True)
df.plot()
result=seasonal_decompose(df['#Passengers'], model='multiplicable',period=12)
result.seasonal.plot()
result.trend.plot()
result.plot()
```
## OUTPUT:
## FIRST FIVE ROWS:
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/81eeb086-9c91-4aae-a06a-2506b9dab925)
## PLOTTING THE DATA:
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/0f4100ba-5747-4a06-9d08-5319f08393a2)
## SEASONAL PLOT REPRESENTATION :
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/5bfaede5-2abf-4c5a-8111-1e308787a473)
## TREND PLOT REPRESENTATION :
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/d5bb2ba3-119c-4e76-b59e-e1603e32ebb2)
## OVERAL REPRESENTATION:
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/b54465cb-a013-46d3-9655-0005df029bd0)
![image](https://github.com/Syam-tej/EXP-2--Implementation-of-time-series-analysis-and-decomposition/assets/93427224/28ee30be-3f1f-470e-b81d-f98c83ceebec)
## RESULT:
Thus we have created the python code for the time series analysis and decomposition.







