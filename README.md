# Ex03-Univariate-Analysis
AIM

To perform Univariate EDA on the given data set

Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

ALGORITHM

STEP 1 Import the built libraries required to perform EDA and outlier removal.

STEP 2 Read the given csv file

STEP 3 Convert the file into a dataframe and get information of the data.

STEP 4 Return the objects containing counts of unique values using (value_counts()).

STEP 5 Plot the counts in the form of Histogram or Bar Graph.

STEP 6 Use seaborn the bar graph comparison of data can be viewed.

STEP 7 Save the final data set into the file

PROGRAM:

import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)
EDA - SuperStore.csv


![image](https://user-images.githubusercontent.com/94911373/192078824-6ec9f43a-0d49-4247-b72c-268f62c06c56.png)



Displaying information about Dataset


![image](https://user-images.githubusercontent.com/94911373/192078873-96983e0b-e8f0-42f5-aaa3-67078f47d4a5.png)


![image](https://user-images.githubusercontent.com/94911373/192078879-efe9e46e-d82e-4e3d-a5e8-111118761a9b.png)


![image](https://user-images.githubusercontent.com/94911373/192078897-e98051e9-35f6-4c89-a4d2-377c2245501a.png)






Finding null values and cleaning it:



![image](https://user-images.githubusercontent.com/94911373/192078914-e4c27bbb-8ed2-4421-add3-3de57c1b892c.png)






Value counts of "Postal Code"



![image](https://user-images.githubusercontent.com/94911373/192078953-0ebb219c-7854-44ce-8060-d824e1103612.png)




Distribution of Data

![image](https://user-images.githubusercontent.com/94911373/192078968-25fa06f1-04cb-43ff-af60-dab7916e99d4.png)





Univariate Analysis


![image](https://user-images.githubusercontent.com/94911373/192078995-a0f5c31e-00a5-4d06-a030-216d4ee931da.png)




![image](https://user-images.githubusercontent.com/94911373/192078998-8aa29f5e-0a91-4a71-bc53-b955dbf06811.png)



![image](https://user-images.githubusercontent.com/94911373/192079004-4a082596-03d1-4f05-9e62-149a8d7d99ea.png)






![image](https://user-images.githubusercontent.com/94911373/192079011-6ab82e52-4dbf-4b8a-9f15-273b3f3bd697.png)




![image](https://user-images.githubusercontent.com/94911373/192079019-72242535-d41e-4098-b8fd-d652d5a2c2be.png)







![image](https://user-images.githubusercontent.com/94911373/192079059-e5f7d132-5f0f-4fea-816a-a02e9958b1e6.png)






RESULT:

Thus the program to perform EDA on the given data set is successfully executed

