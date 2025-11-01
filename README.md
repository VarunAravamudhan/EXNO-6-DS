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
 ~~~
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
display(df.head())
~~~
<img width="586" height="261" alt="image" src="https://github.com/user-attachments/assets/2c928727-d40e-49dd-b2e0-2800c872ee67" />

~~~
# 1.Line Plot
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
plt.show()
~~~
<img width="435" height="308" alt="image" src="https://github.com/user-attachments/assets/0d131c73-a5e3-4910-a945-6f7d72b76baf" />

~~~
# 2.Multi Line Plot
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
plt.show()
~~~

<img width="419" height="301" alt="image" src="https://github.com/user-attachments/assets/e04fbe82-37d8-411d-9255-2a88f5815313" />

~~~
# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
plt.show()
~~~

<img width="571" height="395" alt="image" src="https://github.com/user-attachments/assets/59b665e7-d86f-4bc7-bb81-8d572db731eb" />

~~~
# 2.Scatter Plot
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
~~~

<img width="426" height="309" alt="image" src="https://github.com/user-attachments/assets/3d0253ee-b526-446f-9bcb-ebe1cb7a86bc" />

~~~
# 3.Bubble Chart
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
~~~

<img width="442" height="322" alt="image" src="https://github.com/user-attachments/assets/ffdab32c-5f5d-4585-a9c3-8ee55b958890" />

~~~

<img width="442" height="322" alt="image" src="https://github.com/user-attachments/assets/0f545daa-8adb-4444-9425-5e6d783082b3" />

~~~
# TO CAPTURE DISTRIBUTIONS
# 1.Histogram
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
plt.show()
~~~

<img width="468" height="293" alt="image" src="https://github.com/user-attachments/assets/308570b5-fd1d-4f26-8c2a-35cbc8f1c9af" />

~~~
# 2.Box Plot
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
plt.show()
~~~

<img width="508" height="371" alt="image" src="https://github.com/user-attachments/assets/aeddca4a-f9a4-4411-b059-1c50e67e38d5" />

~~~
# 3.Violin Plot
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.show()
~~~

<img width="453" height="287" alt="image" src="https://github.com/user-attachments/assets/2d1375d3-95b4-4832-b67d-9d06f7f4c183" />

~~~
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
~~~

<img width="509" height="377" alt="image" src="https://github.com/user-attachments/assets/b45f2420-01fc-4fa1-9302-d6fbe6b13baa" />

~~~
# 5.Heatmap
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
~~~

<img width="421" height="337" alt="image" src="https://github.com/user-attachments/assets/00d53610-e8c6-4a7c-88f1-b70ea25fdc44" />














# Result:
This experiment has been verified by varun arvamudhan successfully
