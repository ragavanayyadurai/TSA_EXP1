 ### Developed By: Ragavendran A
### Register No: 212222230114
### Date:

# Ex.No: 01A PLOT A TIME SERIES DATA


## AIM:
To Analyze and visualize trends in medal counts for various countries and sports across Summer Olympics from 1986 to 2020.

## ALGORITHM:

1.Load the Summer Olympic Medals dataset.

2.Clean and preprocess the data.

3.Aggregate and analyze medal counts by year and country.

4.Create visualizations to show trends and distributions.

5.Derive insights from the visualizations and trends.

<br />
<br />


## PROGRAM:


```python

import pandas as pd
import matplotlib.pyplot as plt


data = pd.read_csv("/content/Summer_olympic_Medals.csv")


print(data.head())


data_filtered = data[(data['Year'] >= 1986) & (data['Year'] <= 2020)]


medals_by_year = data_filtered.groupby('Year')['Gold'].count()


plt.figure(figsize=(12, 6))
plt.plot(medals_by_year.index, medals_by_year.values, marker='o', linestyle='-')
plt.title('Number of Gold Medals by Year (1986-2020)')
plt.xlabel('Year')
plt.ylabel('Number of Gold Medals')
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()


```
<br />
<br />
<br />
<br />

## OUTPUT:
![image](https://github.com/user-attachments/assets/8556a1af-cb0a-4f33-863d-c381ab6dcacd)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
