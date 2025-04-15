# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: YAMUNA M

RegisterNumber: 212223230248

```python
import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])
```


## Output:
![Image-1](https://github.com/user-attachments/assets/417bb746-8963-42ee-9fc9-aab640e76b22)

![Image-2](https://github.com/user-attachments/assets/908a5c49-f143-4be1-8ecb-5f1b57f89963)

![Image-3](https://github.com/user-attachments/assets/4c29f296-d6d7-4d2b-8d83-7142220b5f94)

![Image-4](https://github.com/user-attachments/assets/711452fa-8b6c-457d-8094-98b08a9ef275)

![Image-5](https://github.com/user-attachments/assets/5ff22ce0-6b32-4a4a-b71b-b8b3528b8464)

![Image-6](https://github.com/user-attachments/assets/adbcbb25-3ac8-491d-b58b-e9287ef60f5a)

![Image-7](https://github.com/user-attachments/assets/6afaee74-ade6-40b5-b39e-f6628b15bac2)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
