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

```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
<img width="808" height="574" alt="image" src="https://github.com/user-attachments/assets/0a8999a1-03aa-4ef4-9658-f8b44fd7294f" />

```
df = sns.load_dataset("tips")
df
```

<img width="681" height="544" alt="image" src="https://github.com/user-attachments/assets/b252fb2f-255b-40d6-ab26-4453a676d3ac" />

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

<img width="831" height="608" alt="image" src="https://github.com/user-attachments/assets/aa50d749-ec1f-4d76-bab2-42e79cafc846" />

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```

<img width="795" height="622" alt="image" src="https://github.com/user-attachments/assets/880fd185-a47d-4620-bc79-5662d415d58d" />

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

<img width="855" height="664" alt="image" src="https://github.com/user-attachments/assets/f929089f-5ed7-4c12-9a8a-a95783495eea" />

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

<img width="827" height="578" alt="image" src="https://github.com/user-attachments/assets/6887e0dc-ad38-4e9a-8625-e6441819c4ee" />

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

<img width="816" height="568" alt="image" src="https://github.com/user-attachments/assets/04e47760-cd06-45cc-b545-511e22549689" />

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

<img width="839" height="612" alt="image" src="https://github.com/user-attachments/assets/e4391e82-992f-41c0-9705-84538bd64549" />

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```

<img width="910" height="330" alt="image" src="https://github.com/user-attachments/assets/d96b1d8c-e860-44bd-91f0-a33b86be9ff5" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```

<img width="949" height="434" alt="image" src="https://github.com/user-attachments/assets/bef41062-5fd9-4bfb-97a0-571584fd9d8f" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

<img width="911" height="600" alt="image" src="https://github.com/user-attachments/assets/27c02a2c-b873-44f9-830a-6315a0bab39a" />

```tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

<img width="846" height="619" alt="image" src="https://github.com/user-attachments/assets/1b775283-af62-404b-909f-e34554b9680f" />

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

<img width="600" height="290" alt="image" src="https://github.com/user-attachments/assets/59b1ecf3-2721-4085-bf95-dcab8e15b9d1" />

```
sns.histplot(data = num_var, kde = True)
```

<img width="792" height="587" alt="image" src="https://github.com/user-attachments/assets/07d5ad08-3913-4fd4-a4d7-48b22303490d" />

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

<img width="828" height="587" alt="image" src="https://github.com/user-attachments/assets/f2f482bd-98c2-4d58-93e0-398118b6b5b4" />

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

<img width="811" height="583" alt="image" src="https://github.com/user-attachments/assets/932c1114-1da1-42a9-a3a9-601cebc6eb70" />

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

<img width="811" height="580" alt="image" src="https://github.com/user-attachments/assets/0be80da2-3ed6-4bbb-8e53-024e23298657" />

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

<img width="715" height="535" alt="image" src="https://github.com/user-attachments/assets/1c67ca6d-cc81-404a-b553-d8caef145ac6" />

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

<img width="935" height="341" alt="image" src="https://github.com/user-attachments/assets/e4dbe29b-2790-408b-9917-e89c32122ffc" />

```

mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

<img width="818" height="356" alt="image" src="https://github.com/user-attachments/assets/e77f15f7-fa2b-4187-9a4a-3e6b1bc5b9c3" />

```
sns.kdeplot(data=mart,x='PassengerId')
```

<img width="865" height="598" alt="image" src="https://github.com/user-attachments/assets/b91bcb61-ec11-4861-bd19-52861818efd4" />

```
sns.kdeplot(data=mart,x='Age')
```

<img width="848" height="589" alt="image" src="https://github.com/user-attachments/assets/e538a724-fdf9-4540-833a-b63249a86376" />


```
sns.kdeplot(data=mart)
```

<img width="793" height="549" alt="image" src="https://github.com/user-attachments/assets/e4606cfe-3b1d-4469-a794-16db03cbb0d3" />

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

<img width="769" height="541" alt="image" src="https://github.com/user-attachments/assets/2186a272-d6b6-484b-9725-a75e154e79da" />

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

<img width="781" height="557" alt="507616730-0bdee5a7-799d-43d3-b712-f8075178b2a3" src="https://github.com/user-attachments/assets/63ab10d2-9a43-4f32-9074-f961ee837409" />


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

<img width="714" height="547" alt="507616927-59056a37-b042-43a4-bbee-4725f45a5f31" src="https://github.com/user-attachments/assets/8ea8ff9a-8d79-4534-ba9a-0ed53b74de86" />

```
hm=sns.heatmap(data=data)
```

<img width="743" height="566" alt="507617055-6f545b93-5d45-4a92-9785-f7fbe5cacf23" src="https://github.com/user-attachments/assets/8bdc4e29-c0f0-45a6-92f2-2091e1a7ac68" />

 # Result:
 
 Thus, all the data visualization techniques of seaborn has been implemented.

# Summery:

Seaborn plots help shape feature engineering. Line and bar plots show trends and group differences, scatterplots reveal relationships, histograms and KDE show skew, boxplots show outliers, and heatmaps show correlations. Using these insights, you can clean missing values, cap extremes, scale numeric fields, encode categories, and add useful ratios or interactions. After that, recheck with the visuals to confirm improvement.
