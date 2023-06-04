# EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET

# AIM:
To Perform Data Science Process on a complex dataset and save the data to a file.

# DATE:

GITHUB LINK:https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET.git

COLAB LINK:https://colab.research.google.com/drive/1SOprWeJNFdulFLZwyeomCz60668UCoG-#scrollTo=Bz9yOnQIbVDE

# ALGORITHM:

## STEP 1 

Read the given data

## STEP 2 

Clean the Data Set using Data Cleaning Process 

## STEP 3 

Apply Feature Generation/Feature Selection Techniques on the data set 

## STEP 4 

Apply EDA /Data visualization techniques to all the features of the data set

# CODE:

DEVELOPED BY: VISWA PRIYA G

REGISTER NUMBER: 212221220061

Cleaning data:

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("/content/FlightInformation.csv")
df

df.head()

df.describe()

df.info()

df.duplicated()

df.isnull().sum()
``` 

Feature generation:

#Binary encoder

```
import category_encoders as ce
be=ce.BinaryEncoder()
ndf=be.fit_transform(df["Airline"])
df = pd.concat([df, be.fit_transform(df["Airline"])], axis=1)
ndf

import category_encoders as ce
be=ce.BinaryEncoder()
ndf=be.fit_transform(df["Source"])
df = pd.concat([df, be.fit_transform(df["Source"])], axis=1)
ndf
```` 

EDA Techniques

TYPES OF BIVARIATE ANALYSIS:

```
1)Numerical

sns.scatterplot (df['Date_of_Journey'],df['Dep_Time'])

2)Numerical & Categorical

sns.barplot (x=dd['Duration'],y=dd['Price'])

sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df)

states=df.loc[:,["Duration","Price"]]
states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")
plt.figure(figsize=(17,7))
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("Duration")
plt.ylabel=("Price")
plt.show()
```

Multivariate Analysis :

```
df.corr()
data = np.random.randint(low = 1, high = 100, size = (10, 10))
print("The data to be plotted:\n")
print(data)
hm = sns.heatmap(data = data)
plt.show()
```

# OUTPUT

Initial dataset

![d1](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/a33702cf-bf8f-4dd7-bda8-c6dc41db6b4e)

![d2](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/7f675cc9-5223-4cda-b0bf-2d818f0b4d37)

![d3](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/019a53b7-fb50-42af-b6ef-8c02deb9d0b0)

![d5](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/12eb30c8-57f3-40e6-8512-4a85e6bc1195)

df.isnull().sum() - post cleaning

![d4](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/b10ba1cc-d0a9-4872-82d5-c9e6afe9755c)

Feature generation

![d6](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/2c171e8e-a406-48c4-bbde-3dd4b7578abf)

![d7](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/743e8745-00fd-4489-bcf3-8358daf8b293)

EDA Analysis

TYPES OF BIVARIATE ANALYSIS:

1) Numerical

![d8](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/5d3b2cb6-be52-432b-be21-c2d8457ad16b)

2)Numerical & Categorical

![d9](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/28d96b41-6bef-423b-a3a1-c322706d5641)

![d10](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/87b10700-3eaf-4c02-9124-0272145b56a9)

![d11](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/f03a6ccc-e65a-4fb3-980b-3bb726719252)

Multivariate Analysis :

![df12](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/553bc434-e21e-4f32-b498-e6e9a0ac4ae1)

![d13](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/abd28ade-e4f9-428f-ace7-561f28d40a01)

![d14](https://github.com/viswapriyaG/EX-10-DATASCIENCE-PROCESS-ON-COMPLEX-DATASET/assets/131427787/d9cd4b9a-074f-4bc1-abd1-cabebb339c46)


# RESULT:

Thus,Data Science Process on a complex dataset has been performed by applying feature generation and EDA techniques and data is saved to a file.
