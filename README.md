# EXNO:6-DATA VISUALIZATION USING SEABORN LIBRARY

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
```
REG NO: 212224110045
NAME:  A PRANEYA
```
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("/content/titanic_dataset (22).csv")
df.head()
```
![image](https://github.com/user-attachments/assets/2f39de68-a893-4682-8e74-fe9830c0a0dc)

# LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/user-attachments/assets/b47376f5-7ceb-450f-8813-0297f5b67cb4)

# MULTI LINE PLOT
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/user-attachments/assets/9748995c-7c7c-4a55-a48d-0f4ea8ac6cf3)

# BAR CHART
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/user-attachments/assets/2e0702b2-fcaf-480f-b824-2c9806327517)

# SCATTER PLOT
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Age vs Fare Scatterplot')
plt.show()
```
![image](https://github.com/user-attachments/assets/2988a802-a9f5-4cd7-ac6d-536b97252b99)

# BUBBLE CHART 
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title(' Age vs Fare-Bubble Chart- Size by Passenger Class')
plt.show()
```
![image](https://github.com/user-attachments/assets/4a2b0c08-aa28-46fa-a3a4-7120bdf76526)

# HISTOGRAM
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/user-attachments/assets/3231bd25-96cd-4eda-921a-3832f1866108)

# BOX PLOT
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/user-attachments/assets/b46a3607-ac5c-486d-82d8-f3e0c1541d12)

# VIOLIN PLOT
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

![image](https://github.com/user-attachments/assets/5ee1f369-ed61-4109-aec2-39c808eca160)
# DENSITY PLOT
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/user-attachments/assets/3b2cab9d-3e91-4f12-88b0-c51e64b8b7a6)
# HEAT MAP
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

![image](https://github.com/user-attachments/assets/5f81cce5-82c9-4e11-a68f-dd62b272a5bc)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
