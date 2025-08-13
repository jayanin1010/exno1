# Name: Jayani N
# Register no: 212224100025


# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

## Coding and Output
          import pandas as pd
          df=pd.read_csv("Data_set.csv")
          df

<img width="1337" height="483" alt="image" src="https://github.com/user-attachments/assets/cad87a7b-559a-49a7-ba72-fc15e200c1c2" />

#creating own dataset

          data={'Name':['aaa','xxx'],'Age':18}
          df1=pd.DataFrame(data)
          df1

<img width="249" height="145" alt="image" src="https://github.com/user-attachments/assets/90f79e51-95c7-48bd-91e6-91f515284a9f" />


          df.info()

          #summary statistics method that provides quick insights into your dataset — like count, mean, std, min, max, percentiles, etc
          df.describe()

<img width="728" height="341" alt="image" src="https://github.com/user-attachments/assets/3734a54f-c7c3-46d1-89e8-9ecc317e90d5" />

<img width="849" height="342" alt="image" src="https://github.com/user-attachments/assets/b2dde505-26e8-4e05-b795-9e3744a8299f" />

          df.shape
          df.head()
          df.tail()

<img width="143" height="47" alt="image" src="https://github.com/user-attachments/assets/5b73d5c2-8bff-40e8-b899-ee5011966ac5" />
<img width="1345" height="244" alt="image" src="https://github.com/user-attachments/assets/c5139ee4-4f53-4df2-afba-b8aecb4c6df5" />
<img width="1312" height="521" alt="image" src="https://github.com/user-attachments/assets/fff61de5-acfa-4b88-9fed-efde8f14a6e2" />

          df.notnull()
<img width="1312" height="504" alt="image" src="https://github.com/user-attachments/assets/2d58f66a-e2c7-45d7-be93-318bfb44a87d" />

          df.dropna(axis=1)
<img width="801" height="511" alt="image" src="https://github.com/user-attachments/assets/8f283488-85ab-4e7c-9126-b16643949e5c" />

          df.dropna(subset='show_name')
<img width="1369" height="736" alt="image" src="https://github.com/user-attachments/assets/accc2431-3636-4939-9777-91d537fd3032" />
          
          df.isnull()
<img width="1258" height="531" alt="image" src="https://github.com/user-attachments/assets/6fc7d2cd-529d-4174-8428-7dc3d9f05760" />

          df.fillna('hello')
<img width="1364" height="505" alt="image" src="https://github.com/user-attachments/assets/17bec9e3-5d24-4548-9a9b-48fafbc8f351" />
          
          df.fillna(df['rating'].mean())
<img width="1391" height="745" alt="image" src="https://github.com/user-attachments/assets/9ac18019-e64e-47c7-8862-061be3005acd" />

          #can use bfill also
          df.fillna(method='ffill')
<img width="1350" height="520" alt="image" src="https://github.com/user-attachments/assets/71479fc1-49ce-4058-a311-7e9f1533b5b1" />

          #used to fill missing values (NaN) in a pandas DataFrame or Series using interpolation techniques — i.e., estimating the missing values based on surrounding data.
          df.interpolate()

<img width="1326" height="500" alt="image" src="https://github.com/user-attachments/assets/572f8ec0-73de-4bc1-b25d-1716338fc175" />

          #uses both rows and columns indexing here
          df.iloc[1:3,1:3]

<img width="491" height="124" alt="image" src="https://github.com/user-attachments/assets/866099ac-1461-4c8d-94ba-d557555879c2" />

          #to count the frequencies of values in data
          df['country'].value_counts()

<img width="386" height="125" alt="image" src="https://github.com/user-attachments/assets/dfe91fad-b750-43af-a947-f56c3ca80715" />

          df.isnull().sum()
<img width="531" height="236" alt="image" src="https://github.com/user-attachments/assets/a7f876a6-c9ec-416a-a401-0edc2319de5f" />

          import seaborn as sns
          sns.heatmap(df.isnull(),yticklabels=False,annot=True)
<img width="850" height="557" alt="image" src="https://github.com/user-attachments/assets/cac031e1-4d0c-4002-9329-8b695fff8192" />

          sns.heatmap(df.isnull(),yticklabels=True,annot=True)
<img width="953" height="562" alt="image" src="https://github.com/user-attachments/assets/6e78a620-93c5-4504-a0c0-e5fc0f334f85" />

          !pip install seaborn
          import scipy.stats as stats
          import seaborn as sns
          import pandas as pd
          df=pd.read_csv("heights.csv")
          print(df)

<img width="408" height="327" alt="image" src="https://github.com/user-attachments/assets/25d19a06-3e38-4956-89ba-cdca5771cace" />


          sns.boxplot(data=df)
<img width="815" height="546" alt="image" src="https://github.com/user-attachments/assets/ec217cb1-6f01-4a24-a3dc-bc41e9ed805f" />

          sns.scatterplot(data=df)
<img width="901" height="548" alt="image" src="https://github.com/user-attachments/assets/627c1fba-6207-4581-bdaa-04c360f0d1f0" />


          max=df['height'].quantile(0.75)
          min=df['height'].quantile(0.25)
          iqr=max-min 
          print(iqr)

<img width="218" height="27" alt="image" src="https://github.com/user-attachments/assets/0327d61e-5afb-4466-9f4b-b64dd4334db1" />

          lb=min-1.5*iqr
          ub=max+1.5*iqr
          outliers=df[(df['height']<lb)|(df['height']>ub)]
          print("Lower bound:",lb)
          print("Upper bound:",ub)
          print("Outliers:",outliers)
<img width="380" height="113" alt="image" src="https://github.com/user-attachments/assets/12b65a68-32e4-4c68-adf9-d0e24a732d28" />

          no_outliers=df[~((df['height']<lb)|(df['height']>ub))]
          print(no_outliers)
<img width="435" height="277" alt="image" src="https://github.com/user-attachments/assets/c79d6077-1227-4bbb-ac7f-fd5eeaf599f5" />

          sns.boxplot(data=no_outliers)
<img width="847" height="556" alt="image" src="https://github.com/user-attachments/assets/17fa85d8-da53-46a7-a84c-d1bc162a6459" />

          sns.scatterplot(data=no_outliers)

<img width="924" height="566" alt="image" src="https://github.com/user-attachments/assets/4730dcf5-0674-4d72-841f-45bbd29f3254" />

          import matplotlib.pyplot as plt
          print(df)
          max=df['height'].quantile(0.75)
          q2=df['height'].quantile(0.5)
          min=df['height'].quantile(0.25)
          iqr=max-min
          lb=min-1.5*iqr
          ub=max+1.5*iqr
          dfs=df[(df['height']>=lb)&(df['height']<=ub)]
          print(df)

<img width="418" height="347" alt="image" src="https://github.com/user-attachments/assets/e053d405-ff4e-4ce5-a352-f1bb6d225d73" />

          import numpy as np
          z=np.abs(stats.zscore(df['height']))
          print(z)
<img width="649" height="55" alt="image" src="https://github.com/user-attachments/assets/a81b971d-69b1-44d4-a0ed-d1c4b65810df" />

          df1=df[z<3]
          print(df1)

<img width="476" height="307" alt="image" src="https://github.com/user-attachments/assets/041c0f42-4d3e-446e-a064-fb49bc5823a9" />

          val=df['height']
          print(val)

<img width="513" height="348" alt="image" src="https://github.com/user-attachments/assets/9f513870-2ae2-45d8-9117-506a2d5a383a" />

# Result

          out=[]
          def outl(val):
              thresh=3
              m=np.mean(val)
              sd=np.std(val)
              for i in val:
                  z=(i-m)/sd
                  if np.abs(z)>thresh:
                      out.append(i)
              return out
          op=outl(val)
          print(op)

<img width="127" height="40" alt="image" src="https://github.com/user-attachments/assets/fc4b5fd3-5f67-4d8e-bc8a-215ee56f41ac" />



          
