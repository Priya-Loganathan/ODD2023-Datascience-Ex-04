# Ex-04-Multivariate-Analysis

## AIM :

To perform Multivariate EDA on the given data set.

## EXPLANATION :

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM :

STEP1
Import the built libraries required to perform EDA and outlier removal.

STEP2
Read the given csv file.

STEP3
Convert the file into a dataframe and get information of the data.

STEP4
Return the objects containing counts of unique values using (value_counts()).

STEP5
Plot the counts in the form of Histogram or Bar Graph.

STEP6
Use seaborn the bar graph comparison of data can be viewed.

STEP7
Find the pairwise correlation of all columns in the dataframe.corr() .

STEP8
Save the final data set into the file.

## PROGRAM:

Developed by : DELLI PRIYA L
Register number : 212222230029
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

data=pd.read_csv("SuperStore.csv")
data

data.head()

data.info()

data.describe()

data.isnull().sum()

data.dtypes

sns.scatterplot(data['Postal Code'],data['Sales'])

states=data.loc[:,["State","Sales"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES")
plt.ylabel=("SALES") 
plt.show()

states=data.loc[:,["State","Postal Code"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Postal Code",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES") 
plt.ylabel=("Postal Code") 
plt.show()

states=data.loc[:,["Segment","Sales"]] 
states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(10,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("SEGMENT") 
plt.ylabel=("SALES") 
plt.show()

sns.barplot(data['Postal Code'],data['Ship Mode'],hue=data['Region'])

data.corr()

sns.heatmap(data.corr(),annot=True)
```

## OUTPUT :

### DATASET
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/88cf4c6a-8a12-489c-87f1-2ad16f2dd4d2)
### HEAD DATA
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/fdc83672-fa36-4942-a264-09f5927b15a7)
### INFORMATION
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/8dc081c4-44e8-4443-a435-2c7d08a57dac)
### DESCRIPTION
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/a092338f-82ea-4685-b894-be83a525981a)
### DATATYPE
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/0f450ad9-5dfb-446d-82c8-2c2d3ef5243a)
### NULL DATA
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/e33541b1-b21d-4b61-8ced-6993d3ee67ce)
### SCATTER PLOT
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/999d6695-a7b0-4578-a083-bd3402dd3796)
### BAR PLOT - State and Sales
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/43f52f4d-be40-4348-bee6-8d08c66140c2)
### BAR PLOT - State and Postal code
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/24409676-3470-4334-98b5-2c56dc7fc51a)
### BAR PLOT- Segment and Sales
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/62ab3124-b78e-4210-b225-16fde8ee189f)
### BAR PLOT - Postal code and Ship mode
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/cc171a1c-8da1-49d4-bb4a-63c719a468ce)
### CORRELATION COEFFICIENT
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/3b1ebf6a-4074-49f1-af7a-d0f72a7071d1)
### HEATMAP
![image](https://github.com/Priya-Loganathan/ODD2023-Datascience-Ex-04/assets/121166075/b2fa83c5-2344-42b9-b265-9f46704a6d4d)

## RESULT:
Thus the program to perform Multivariate EDA on the given data set is successfully executed.










