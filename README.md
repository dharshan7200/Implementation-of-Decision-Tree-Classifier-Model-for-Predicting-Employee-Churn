# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Load and inspect the dataset (Employee.csv) to understand its structure and check for missing values.
   
2. Encode categorical variables, such as "salary," to prepare the data for modeling.
   
3. Split the data into training and testing sets with an 80-20 ratio.

4. Train a DecisionTreeClassifier using the "entropy" criterion on the training data.

5. Evaluate model accuracy and make predictions on test data and a sample input.


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: DHARSHAN D
RegisterNumber: 212223230045

import pandas as pd
data=pd.read_csv("Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["salary"]=le.fit_transform(data["salary"]) 
data.head()

x=data[["satisfaction_level", "last_evaluation", "number_project", "average_montly_hours", "time_spend_company", "Work_accident", "promotion_last_5years", "salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split 
x_train,x_test,y_train, y_test=train_test_split(x,y, test_size=0.2, random_state=100)

from sklearn.tree import DecisionTreeClassifier

dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train) 
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred) 
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]]) 
*/
```

## Output:
## DATA HEAD
![SS1](https://user-images.githubusercontent.com/115924983/200124488-77dbf1c7-6c9b-4fb8-9f0b-b3cb762caedd.png)

## DATA INFO
![SS2](https://user-images.githubusercontent.com/115924983/200124505-b2db3dd5-48e9-41e0-8d47-877ceda29d32.png)

## DATA ISNULL
![SS3](https://user-images.githubusercontent.com/115924983/200124524-691cd13c-a57f-43c5-8f28-bf71c3fe21c9.png)

## DATA LEFT
![SS4](https://user-images.githubusercontent.com/115924983/200124541-49e1d70e-fa4d-43a3-83d6-ce07717a061a.png)

## X HEAD
![SS5](https://user-images.githubusercontent.com/115924983/200124554-37ee7083-8de7-419a-947b-361e2cec703e.png)

## DATA FIT
![SS6](https://user-images.githubusercontent.com/115924983/200124575-fda6203d-da17-4781-b79c-ea4f6b717d4e.png)

## ACCURACY
![SS7](https://user-images.githubusercontent.com/115924983/200124598-d38e91c4-c3a2-4714-98d2-c29bbf82b92b.png)

## PREDICTED VALUES
![SS8](https://user-images.githubusercontent.com/115924983/200124634-33187054-9870-428b-b3af-40aa5e71fc7f.png)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
