 ### Developed By: Ragavendran A
### Register No: 212222230114
### Date:

# Ex.No: 01A PLOT A TIME SERIES DATA


## AIM:
To analyze and visualize air quality data over time, focusing on pollutant levels such as NOx(GT), and identifying patterns or trends.

## ALGORITHM:

# Step 1:
Import the dataset into a DataFrame.

# Step 2:
Convert date columns to datetime format and handle missing values.

# Step 3:
Identify and select relevant features for analysis.

# Step 4:
Perform exploratory data analysis to understand trends and patterns.

# Step 5:
Apply appropriate statistical or machine learning models for forecasting or classification.

# Step 6:
Plot the results to visualize trends, anomalies, and predictions.

<br />
<br />


## PROGRAM:


```python

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

sns.set(style="darkgrid")


df = pd.read_csv('/content/Air Quality.csv')

df['Date'] = pd.to_datetime(df['Date'], dayfirst=True)

df.set_index('Date', inplace=True)

df = df.dropna(subset=['NOx(GT)'])

plt.figure(figsize=(12, 6))
plt.plot(df.index, df['NOx(GT)'], marker='o', linestyle='-', color='blue', label='NOx(GT) Concentration')

plt.title('NOx(GT) Concentration Over Time', fontsize=16)
plt.xlabel('Date', fontsize=12)
plt.ylabel('NOx(GT) Concentration (µg/m³)', fontsize=12)


plt.legend()

plt.show()
```
<br />
<br />
<br />
<br />

## OUTPUT:
![image](https://github.com/user-attachments/assets/8cdf4912-7ee4-420c-99a9-388b46a8f3dc)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
