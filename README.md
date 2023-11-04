# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the required libraries .

2.Read the data frame using pandas.

3.Get the information regarding the null values present in the dataframe.

4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.

5.Determine training and test data set.

6.Apply decision tree regression on to the dataframe.

7.Get the values of Mean square error, r2 and data prediction.  

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SHALINI.K
RegisterNumber:  212222240095
data=pd.read_csv("Salary Data.csv")
data.head()
data.tail()
data.info()
data["Gender"]=data["Gender"].astype('category')
data["Education Level"]=data["Education Level"].astype('category')
data["Job Title"]=data["Job Title"].astype('category')
data.info()
data["Gender"]=data["Gender"].cat.codes
data["Education Level"]=data["Education Level"].cat.codes
data["Job Title"]=data["Job Title"].cat.codes
data.info()
data.head()
x=data[['Age','Gender','Education Level','Job Title','Years of Experience']]
x
x.shape
y=data[['Salary']]
y.shape
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeRegressor
dtr=DecisionTreeRegressor()
dtr.fit(x_train,y_train)
y_pred=dtr.predict(x_test)
print(y_pred)
x_train.shape
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dtr.predict([[44,0,2,130,20]])
```

## Output:

# READ CSV HEAD FILE:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/3ffb504d-a7a1-4b42-b749-0f3258bcf656)

# TAIL:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/79f6f7b2-e790-4c46-9b7b-f571c25ede2f)

# DATASET INFO:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/271d7609-b28e-4831-8171-6c39b47a5d20)

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/f73952ba-feef-4e59-b81b-641792c23306)

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/d3f6e59b-b67d-414c-a0cd-9ce4e5299dc4)

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/fbab1c96-a847-49e5-9506-4f00c69fa18e)

# X DATA:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/87c15651-41cf-479b-ae52-02199bca48d2)

# DATA SHAPE:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/b13e6c8c-9715-4102-be85-56028ac0ad1b)

# Y PRED:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/674e7856-c6c6-4897-8ad2-d4ac3827c18f)

# MEAN SQUARED VALUE:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/ff568d12-9386-458b-8798-27dc71ba0ceb)

# R2 VALUE:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/f41bcce2-bce0-460f-970a-d4401fb4b4bf)

# DTR PREDICT:

![image](https://github.com/shalinikannan23/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118656529/557c20fa-1ba0-43c1-a323-41cbed452f87)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
