# EXNO2DS
# Name: Vikaash P
# Reg no : 212223240180
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT:
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv('titanic_dataset.csv')
df
```
<img width="1221" height="429" alt="image" src="https://github.com/user-attachments/assets/a9d20cc3-5330-4552-ba08-a358c6b05d3c" />

```
df.info()
```
<img width="489" height="413" alt="image" src="https://github.com/user-attachments/assets/3d1cb87a-68a2-41f8-a2dd-2c1fae884cd1" />
```
df.describe()
```
<img width="741" height="295" alt="image" src="https://github.com/user-attachments/assets/41bb24ec-5c6e-4858-a3b2-5a1d9a426d9a" />

```
df.dtypes
```
<img width="280" height="281" alt="image" src="https://github.com/user-attachments/assets/e1d303d7-e352-408e-85f3-da79f015f9b1" />

df.shape

<img width="139" height="25" alt="image" src="https://github.com/user-attachments/assets/7d140f37-4ba5-4f20-add0-49ccb0102aa6" />

df.value_counts()

<img width="1246" height="543" alt="image" src="https://github.com/user-attachments/assets/f76f8e22-04e7-4c6e-8d3e-c2e16f1a13ed" />
```
df['Age'].value_counts()
```
<img width="383" height="266" alt="image" src="https://github.com/user-attachments/assets/6a9b7697-b460-4435-91a9-4798edcd7278" />
```
df.set_index("PassengerId",inplace=True)
df
```
<img width="1232" height="469" alt="image" src="https://github.com/user-attachments/assets/10c92b1d-5c69-404f-8e99-4cedfa1fc966" />
```
df.nunique()
```
<img width="188" height="259" alt="image" src="https://github.com/user-attachments/assets/14f69fce-e0ed-4529-bbeb-dc66894eb264" />
```
sns.countplot(data=df,x="Age")
```
<img width="919" height="584" alt="image" src="https://github.com/user-attachments/assets/e88cde45-02f9-4cb1-83d0-0f959ca1e034" />
```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
<img width="1230" height="470" alt="image" src="https://github.com/user-attachments/assets/ac44432b-aee5-4a40-8a36-8082c01a52dc" />
```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
```
<img width="1043" height="663" alt="image" src="https://github.com/user-attachments/assets/a20fe3e7-a529-4282-b510-753307fcb492" />
```
df.boxplot(column="Age",by="Survived")
```
<img width="818" height="615" alt="image" src="https://github.com/user-attachments/assets/a9ab76c6-2786-4d2d-b038-ddf78efe728b" />
```
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
<img width="897" height="570" alt="image" src="https://github.com/user-attachments/assets/7ddd21b1-2fc8-4a8c-a26a-c0653c2ead9c" />
```
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```
<img width="1007" height="538" alt="image" src="https://github.com/user-attachments/assets/f5bdf909-a40c-4ad6-8682-5dd8efeff8c5" />
```
sns.catplot(x="Pclass",y="Age",col="Survived",hue="Gender",kind="box",data=df)
```
<img width="1234" height="598" alt="image" src="https://github.com/user-attachments/assets/0afce470-348e-4273-9008-10939d912b49" />
```
corr = df.corr(numeric_only=True)
sns.heatmap(corr, annot=True)
```
<img width="790" height="573" alt="image" src="https://github.com/user-attachments/assets/7fb474f6-8eb2-422d-b860-7df2f1b844b2" />

# RESULT
Exploratory Data Analysis is performed successfully on the given dataset.
