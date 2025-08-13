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




# Result
          <<include your Result here>>
