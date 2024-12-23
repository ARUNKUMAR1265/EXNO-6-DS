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
from google.colab import drive
drive.mount('/content/drive')

import seaborn as sns
import matplotlib.pyplot as plt

x=[1,2,3,4,5]
y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

![Screenshot 2024-12-23 101939](https://github.com/user-attachments/assets/53360630-6b59-44f7-b343-b781acecb3f4)

df=sns.load_dataset("tips")

df

![Screenshot 2024-12-23 101950](https://github.com/user-attachments/assets/4b0ce552-1cf3-4e66-9813-ffcfb5d60857)

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")

![Screenshot 2024-12-23 101959](https://github.com/user-attachments/assets/1db712ef-959d-4701-9ab1-fc92db8cad31)

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title("Multi-line Plot")

plt.xlabel('x-axis')

plt.ylabel('y-axis')

![Screenshot 2024-12-23 102009](https://github.com/user-attachments/assets/9653779c-6a7c-4d04-bd76-b7e9083326f9)

import seaborn as sns

import matplotlib.pyplot as plt

tips=sns.load_dataset("tips")

avg_total_bill=tips.groupby('day')['total_bill'].mean()

avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')

plt.xlabel('Day of the week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

![Screenshot 2024-12-23 102027](https://github.com/user-attachments/assets/8fd32f5a-6a78-4abb-bbb9-7c3a31519543)


avg_total_bill=tips.groupby('time')['total_bill'].mean()

avg_tip=tips.groupby('time')['tip'].mean()

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)

plt.xlabel('Time of Day')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Time of Day')

plt.legend()

![Screenshot 2024-12-23 102040](https://github.com/user-attachments/assets/98197a06-f95e-4129-b15c-7e79a0d4add5)

years=range(2000, 2012)

apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]

oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]

plt.bar(years, apples)

plt.bar(years, oranges, bottom=apples)

![Screenshot 2024-12-23 102050](https://github.com/user-attachments/assets/4e821a92-3a2c-4978-b1fb-c5ce23ee049e)

import seaborn as sns

dt=sns.load_dataset('tips')

sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')

plt.xlabel('Day of the week')

plt.ylabel('Total Bill')

plt.title('Total Bill by Day and Gender')

![Screenshot 2024-12-23 102101](https://github.com/user-attachments/assets/bb3b8080-e934-4848-8a75-90e7dd469c19)

ls drive/MyDrive/titanic_dataset.csv

![Screenshot 2024-12-23 102112](https://github.com/user-attachments/assets/cca1d840-6776-47ec-8371-3438d99c0567)

import pandas as pd

tit=pd.read_csv("drive/MyDrive/titanic_dataset.csv")

tit

![Screenshot 2024-12-23 102126](https://github.com/user-attachments/assets/eb2ae94e-3756-42a6-bbe6-af013da3aa82)

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")

![Screenshot 2024-12-23 102141](https://github.com/user-attachments/assets/cb8baa8b-c7ed-43f2-bb5b-eb0a46fbe16d)

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')

plt.title("Age of Passenger by Embarked Town,Divided by Class")

![Screenshot 2024-12-23 102155](https://github.com/user-attachments/assets/660dcd03-4a11-43e1-a0f3-89335c826253)

import seaborn as sns

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)

plt.xlabel('Total Bill')

plt.ylabel('Tip Amount')

plt.title('Scatter Plot of Total Bill vs Tip Amount')

![Screenshot 2024-12-23 102202](https://github.com/user-attachments/assets/3cb7bcb2-845c-404d-890a-b5fb7c88e14d)

import numpy as np

import pandas as pd

np.random.seed(1)

num_var=np.random.randn(1000)

num_var=pd.Series(num_var,name="Numerocal Variable")

num_var

![Screenshot 2024-12-23 102208](https://github.com/user-attachments/assets/553605b6-6a20-4749-aaf2-fd799dadfcf9)

sns.histplot(data=num_var,kde=True)

![Screenshot 2024-12-23 102214](https://github.com/user-attachments/assets/1d6659ff-789c-4315-9094-15cca29d1b80)

df=pd.read_csv("drive/MyDrive/titanic_dataset.csv")

df

![Screenshot 2024-12-23 102228](https://github.com/user-attachments/assets/8d57aeff-de8c-4d13-abc4-f7af3caae677)

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

![Screenshot 2024-12-23 102236](https://github.com/user-attachments/assets/70f4f40c-9588-4d45-bfe1-6c31a8728ef7)

import seaborn as sns

import matplotlib.pyplot as plt

np.random.seed(0)

marks=np.random.normal(loc=70,scale=10,size=100)

marks

![Screenshot 2024-12-23 102243](https://github.com/user-attachments/assets/0e9afd5f-2ea3-4621-ac51-1629efa358f8)

sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)

plt.xlabel('Marks')

plt.ylabel('Density')

plt.title('Histogram of Students Markds')

![Screenshot 2024-12-23 102255](https://github.com/user-attachments/assets/1307a6f5-e5c9-495c-87b7-4987fc5a6d9a)

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])

![Screenshot 2024-12-23 102304](https://github.com/user-attachments/assets/da93e67c-3abd-4c33-8574-c3a38a1f7219)

sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
            
![Screenshot 2024-12-23 102312](https://github.com/user-attachments/assets/49a8d9e2-502b-4b13-8fbf-e25350581914)

sns.boxplot(x="Pclass",y="Age",data=df,palette='rainbow')

plt.title("Age by Passenger Class, Titanic")

![Screenshot 2024-12-23 102326](https://github.com/user-attachments/assets/5cd84cc6-3864-42a2-9bfc-9e2201849fe8)

sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,
palette='Set3',inner="quartile")

plt.xlabel("Day of the week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")

![Screenshot 2024-12-23 102335](https://github.com/user-attachments/assets/5e730cce-91ce-4656-87ae-624fe0e33fbd)

import seaborn as sns

sns.set(style='whitegrid')

tip=sns.load_dataset('tips')

sns.violinplot(x='day',y='tip',data=tip)

![Screenshot 2024-12-23 102343](https://github.com/user-attachments/assets/ee9baa8d-ed76-4a84-a2e5-bda58a0897c7)

tip=sns.load_dataset('tips')

sns.violinplot(x=tip["total_bill"])

![Screenshot 2024-12-23 102355](https://github.com/user-attachments/assets/021cf4a7-e775-4227-812f-9d133bec1440)

sns.set(style='whitegrid')

tips=sns.load_dataset("tips")

sns.violinplot(x='tip',y='day',data=tip)

![Screenshot 2024-12-23 102406](https://github.com/user-attachments/assets/ca6d5759-8d9a-4554-8c59-ba6b6bb23479)

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)

multiple='stack'

multiple='layer'

![Screenshot 2024-12-23 102413](https://github.com/user-attachments/assets/1549a81b-bcd2-4277-a544-fddfc5f69e54)

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)

![Screenshot 2024-12-23 102421](https://github.com/user-attachments/assets/26007d14-dad0-40e1-b327-930e8496ab2c)

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)

![Screenshot 2024-12-23 102429](https://github.com/user-attachments/assets/b828e43c-0e2d-4f0c-b94b-955f3eacaf1a)

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set2',alpha=0.8)

![Screenshot 2024-12-23 102437](https://github.com/user-attachments/assets/1d5ad281-b61b-4a2e-8fe6-dab82cd69241)

mart=pd.read_csv("drive/MyDrive/supermarket.csv")

mart

![Screenshot 2024-12-23 102457](https://github.com/user-attachments/assets/5264c323-f7d5-4380-8123-89e4262f0cb1)

sns.kdeplot(data=mart,x='Total')

![Screenshot 2024-12-23 102508](https://github.com/user-attachments/assets/bc8293ce-f619-430a-a4e9-63fe6348f32e)

sns.kdeplot(data=mart,x='Unit price')

![Screenshot 2024-12-23 102513](https://github.com/user-attachments/assets/cbad3bdc-72a4-4eeb-a917-193a627b8d95)

sns.kdeplot(data=mart)

![Screenshot 2024-12-23 102519](https://github.com/user-attachments/assets/e063bf97-95ed-4609-b0f7-7e5b2d0ffeab)

sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

![Screenshot 2024-12-23 102527](https://github.com/user-attachments/assets/02cf978c-f2ce-47c6-a8cb-686028775563)

sns.kdeplot(data=mart,x='Unit price',y='gross income')

![Screenshot 2024-12-23 102536](https://github.com/user-attachments/assets/f4359fe5-38d6-43fe-b449-5e4ab2837f85)

data=np.random.randint(low=1,high=100,size=(10,10))

print("The data to be plotted:\n")

print(data)

![Screenshot 2024-12-23 102545](https://github.com/user-attachments/assets/a0eeae6b-1bac-487a-b1ee-92549223abb6)

hm=sns.heatmap(data=data,annot=True)

![Screenshot 2024-12-23 102554](https://github.com/user-attachments/assets/1077732c-af57-4aa9-8c4b-4c7ab77e915e)

hm=sns.heatmap(data=data)

![Screenshot 2024-12-23 102600](https://github.com/user-attachments/assets/8fb0c573-cd02-44d0-af90-f5cf4e6fd5b2)

tips=sns.load_dataset("tips")

numeric_cols=tips.select_dtypes(include=np.number).columns

corr=tips[numeric_cols].corr()

sns.heatmap(corr,annot=True,cmap="plasma",linewidths=0.5)

![Screenshot 2024-12-23 102607](https://github.com/user-attachments/assets/0f0667c6-6c5c-4b65-b41d-6994d3807200)

# Result:
The code is run successfully.
