# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE

import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.isnull()

df.isnull().sum()

# OUPUT
![image](https://user-images.githubusercontent.com/118671457/226087844-b79c8054-10d9-4dbb-85a2-a8e15465a9e1.png)
![image](https://user-images.githubusercontent.com/118671457/226087862-d84f8838-81e8-4ca5-bb5d-d9219e8f364b.png)
![image](https://user-images.githubusercontent.com/118671457/226087874-18f27244-3a78-4295-be85-75f74e2eff88.png)
![image](https://user-images.githubusercontent.com/118671457/226087898-b07ec42c-a5f2-417d-b427-85d4f1bf4a3e.png)
![image](https://user-images.githubusercontent.com/118671457/226087918-f76591ab-aa24-4c5e-9539-0bd974ad6749.png)
![image](https://user-images.githubusercontent.com/118671457/226087944-28cd8562-beb4-429a-a4cd-fb7228037e47.png)
![image](https://user-images.githubusercontent.com/118671457/226087988-6054caee-9550-4543-9773-dd34ff1294e8.png)

Result:

Thus,the given data is read,cleaned and the cleaned data is saved into the file.
