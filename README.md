# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Name: PAMURU VENKATESH
Reg.no: 212224040230
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1406" height="324" alt="Screenshot 2025-10-23 141952" src="https://github.com/user-attachments/assets/225f09f6-f4d8-408b-b304-74a693a8d4fc" />


### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="942" height="578" alt="Screenshot 2025-10-23 142014" src="https://github.com/user-attachments/assets/b450f847-6b1d-49c3-9f74-efb3ac08f04b" />

### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="958" height="585" alt="Screenshot 2025-10-23 142049" src="https://github.com/user-attachments/assets/ba759806-0af4-4115-a428-45432aaf61d6" />


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1404" height="745" alt="Screenshot 2025-10-23 142132" src="https://github.com/user-attachments/assets/191bfeae-8416-45ca-99e1-e0f37cae90f7" />

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="970" height="586" alt="Screenshot 2025-10-23 142159" src="https://github.com/user-attachments/assets/0846315b-8985-45e3-bce8-88756b55d808" />

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="955" height="586" alt="Screenshot 2025-10-23 142222" src="https://github.com/user-attachments/assets/79ee62d0-844b-4e27-a43e-83e39f0aaf6a" />

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="975" height="579" alt="Screenshot 2025-10-23 142249" src="https://github.com/user-attachments/assets/7c9f5575-7e43-44b7-b6d4-c742ecac4154" />

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1418" height="730" alt="Screenshot 2025-10-23 142314" src="https://github.com/user-attachments/assets/e0135bd0-ef00-471b-b618-65b74fc416cd" />

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="896" height="590" alt="Screenshot 2025-10-23 142336" src="https://github.com/user-attachments/assets/faf6ee53-2d6c-4bad-8f21-f47429689cab" />

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="918" height="559" alt="Screenshot 2025-10-23 142356" src="https://github.com/user-attachments/assets/1e147c27-1a8b-43c0-82cc-c789ed688b02" />

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="1007" height="643" alt="Screenshot 2025-10-23 142419" src="https://github.com/user-attachments/assets/0ae704ff-cc60-4257-a4b7-0003918b0c1e" />


## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

