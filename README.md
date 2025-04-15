# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df=pd.read_csv("titanic_dataset.csv")

df.head()

![Screenshot 2025-04-15 112626](https://github.com/user-attachments/assets/1c14ae1e-5b45-449d-83b6-7501d5bfbb76)
## 1.Line Plot

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

plt.title('Line Plot')

![Screenshot 2025-04-15 112706](https://github.com/user-attachments/assets/067067e7-39c6-4429-a0df-da048dc1d765)
## 2.Multi Line Plot

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title('Multi Line Plot')

![Screenshot 2025-04-15 112741](https://github.com/user-attachments/assets/af9c34a9-3e72-408b-b193-e210ea7179e4)
## TO VISLUALIZE RELATIONSHIP 1.Bar Chart

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')

plt.title("Fare Of Passenger By Embarked Town")

![Screenshot 2025-04-15 113149](https://github.com/user-attachments/assets/4ba87e7d-872f-4ac6-8fcf-587045239952)

## 2.Scatter Plot

sns.scatterplot(x="Age", y="Fare", data=df)

plt.title('Scatterplot of Age vs Fare')

plt.show()

![Screenshot 2025-04-15 113252](https://github.com/user-attachments/assets/6b79a161-0a1c-40ad-9975-a1240c16c9ab)

## 3.Bubble Chart

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))

plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')

plt.show()

![Screenshot 2025-04-15 113405](https://github.com/user-attachments/assets/5b420274-58be-4645-9c09-2adcdaf31649)

## TO CAPTURE DISTRIBUTIONS 1.Histogram

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

![Screenshot 2025-04-15 113507](https://github.com/user-attachments/assets/c3420982-c590-4105-ac1d-48d3db121adb)

## 2.Box Plot

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')

plt.title("Age By Passenger Class")

![Screenshot 2025-04-15 113547](https://github.com/user-attachments/assets/37c14920-208e-418b-82b1-a46dee7eb060)

## 3.Violin Plot

sns.violinplot(x="Pclass", y="Fare", data=df)

plt.title('Violin Plot of Fare by Passenger Class')

plt.show()

![Screenshot 2025-04-15 113639](https://github.com/user-attachments/assets/cfbc9643-c0e7-4cfd-8a25-1416dd0afbda)

## 4.Density Plot

sns.kdeplot(data=df['Age'], shade=True)

plt.title('Density Plot of Passenger Ages')

plt.show()

![Screenshot 2025-04-15 113730](https://github.com/user-attachments/assets/3d67b43b-4415-4a1d-a067-dc734db176c3)

## 5.Heatmap

numeric_df = df.select_dtypes(include=['float64', 'int64'])

corr_matrix = numeric_df.corr()

sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')

plt.title('Heatmap of Titanic Dataset')

plt.show()

![Screenshot 2025-04-15 113817](https://github.com/user-attachments/assets/3219c914-bbb3-40c1-91dd-760d18e1ec55)

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
