# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import dataset and get data info


2.check for null values


3.Map values for position column


4.Split the dataset into train and test set


5.Import decision tree regressor and fit it for data


6.Calculate MSE,R2 and y predict.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: DIVAKAR R 
RegisterNumber: 212222240026

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
l0=LabelEncoder()

data["Position"]=l0.fit_transform(data['Position'])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
*/
```

## Output:

data.head()

![ml701](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/f7a9ddb8-af0d-4c20-b338-949087a2469a)


data.info()



![ml702](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/9d761fbf-29d7-41be-bdc9-543533968b28)


isnull() and sum()


![ml703](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/d9764897-bae4-48e8-93e4-6a957e963ef1)


data.head() for salary


![ml704](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/12dc80f5-0451-4748-b7ca-4211d10a1818)


MSE value


![ml705](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/55524fc1-1128-449b-bbb0-28a987186fbb)


r2 value



![ml706](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/8e7b47d6-17a3-4ef3-93df-6b17fde9fcbb)


data prediction


![ml707](https://github.com/divakar618/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121932143/5a707832-3c43-4527-9145-8deee6b4e6a1)





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
