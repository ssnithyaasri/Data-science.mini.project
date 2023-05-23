# Data-science.mini.project
# DATA ANALYSIS
# AIM:

To Perform Data Analysis on the given dataset and save the data to a file.

# Explanation

Data analytics is important because it helps businesses optimize their performance.Implementing it into the business model means companies can help reduce costs by identifying more efficient ways of doing business and by storing large amounts of data

# ALGORITHM
# STEP 1
Read the given Data

# STEP 2
Clean the Data Set using Data Cleaning Process

# STEP 3
Apply Feature generation and selection techniques to all the features of the data set

# STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/ds_salaries.csv",encoding="ISO-8859-1")
dfdf.isnull()
df.info()
df.describe()
sns.lineplot(x="work_year",y="salary",data=df,marker='o')
plt.title("work_year vs salary")
plt.xticks(rotation = 90)
plt.show()

sns.barplot(x="work_year",y="salary",data=df)
plt.xticks(rotation = 90)
plt.show()
df.shape
df1 = df[(df.salary>= 60)]
df1.shape

plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
sns.lineplot(x="company_size",y="salary",data=df)
plt.show()
states=df.loc[:,["work_year","salary"]]
states=states.groupby(by=["work_year"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("work_year")
plt.ylabel=("salary")
plt.show()
df.groupby(['work_year']).sum().plot(kind='pie', y='salary',figsize=(6,9),pctdistance=1.7,labeldistance=1.2)
df["work_year"].corr(df["salary"])
df_corr = df.copy()
df_corr = df_corr[["work_year","salary"]]
df_corr.corr()
sns.pairplot(df_corr, kind="scatter")
plt.show()
grouped_data = df.groupby('employment_type')[['work_year', 'salary']].mean()
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
ax.bar(grouped_data.index, grouped_data['work_year'], label='work_year')
ax.bar(grouped_data.index, grouped_data['salary'], bottom=grouped_data['work_year'], label='salary')
ax.set_xlabel('employment_title')
ax.set_ylabel('Value')
ax.legend()
plt.show()
grouped_data = df.groupby(['job_title', 'company_size'])[['work_year', 'salary']].mean()
pivot_data = grouped_data.reset_index().pivot(index='job_title', columns='company_size', values=['work_year', 'salary'])
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
pivot_data.plot(kind='bar', ax=ax)
ax.set_xlabel('job_title')
ax.set_ylabel('Value')
plt.legend(title='company_size')
plt.show()

```

OUTPUT:

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/9fdb8b84-e38f-41f4-9cd5-07a3f6e37d97)
![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/f13bef44-da31-4401-8c7b-ec92ed002112)
![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/3c06dd9a-f734-48b3-969d-25c4e2d0cb02)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/57b17146-637b-4ade-9a91-17ff87efce89)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/991d8f56-c2b0-4b5e-90be-bb7a231ed217)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/cf57e4a8-68df-4ae8-b45e-eab71c1660b2)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/2147e845-e0ab-4813-9f02-68c0805072b0)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/c5c5a423-8928-463c-bc73-9011ecd6fe80)
![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/04454e92-e8fe-494a-a2f6-d2e4326c2c91)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/5cd50788-67f1-4efb-99ae-5ce92fdbba4b)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/7257eef1-6935-4753-b471-ae55336f392c)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/def0f1cb-d636-4267-98aa-b851a284013b)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/888ae9ce-14ca-4cfe-a69e-f7fe307cf2cd)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/4b9fcf62-0f1c-47bc-9ddc-ba0c3e682074)
![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/42913042-7d2d-4446-8837-68d1c8512088)

![image](https://github.com/ssnithyaasri/Data-science.mini.project/assets/119122478/44c02321-578f-40d6-b9b4-182915227685)

# Result:
Thus, Data analysis is performed on the given dataset and save the data to a file



