# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print (df)
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/d3943504-7d06-40c6-a42a-b9d33a2f2542)
df.head(10)
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/ab88e21f-161b-4d9d-9123-9b4764edbd64)
df.info()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/d12ab23c-9112-4a7a-9ae0-2a56fc50e162)
df.isnull()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/82105415-c112-40aa-9ace-b07c4bc3024a)
df.isnull().sum()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/e4eb12ec-e7e7-4a34-a08b-f508b63982b3)
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/226762ab-d302-4b38-a6f7-6dd12b07fe42)
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/65d8d85f-8e88-4a95-8395-d934bd53fc86)
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/a47c42bb-40c3-49d7-abd7-4ab9d9e9e95e)
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/1846face-5de3-4ef8-a7cd-0ceca7d05a3a)
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/28c928ba-a8dc-4e85-a803-dd8de0072b35)
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/05ac82ac-53c7-416b-9900-a80a6fd28647)



import pandas as pd
df=pd.read_csv("Loan_data.csv")
print (df)
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/114ea423-6bc0-4a82-8769-ce3ae102772b)
df.head(10)
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/00b5fe37-e676-4622-861f-14a6f33c0ef5)
df.info()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/54ff8bd2-9bd2-4da5-9824-a00072610476)
df.isnull()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/744f80aa-f4c7-4d4f-a747-72b4fdf9c22c)
df.isnull().sum()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/3127b10f-92e4-4d26-9b8f-0a5bd8251747)
df['Loan_ID']=df['Loan_ID'].fillna(df['LoanAmount'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/a0e4a84d-5f29-4acc-abd3-f8a10d4b5137)
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/4183e39f-08f2-4225-8e93-eb1d80082586)
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/910cc9d9-9788-4fc7-b73b-ee1e4e084a1d)
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/0447c815-fc02-4f4c-8c93-37b55b894542)
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/57870818-061b-4e30-b0df-814da8ee9181)
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/62ed5b96-5315-4cbc-a587-d57fae0dbe3b)
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
```
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/beabdc8a-656f-4a7c-a088-5dc1daf5daef)
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].mean())
df.head()
```
![image](https://github.com/Vaish-1011/ODD2023-Datascience-Ex01/assets/135130074/a46cde82-e89f-4d77-b307-53427c3d1af8)



