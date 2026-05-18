# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import pandas
2. imort decision tree classifier
3. Fit the data in the model
4. Find the accuracy code

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: m.p.dhanalakshmi
RegisterNumber: 212225040063
import pandas as pd
data=pd.read_csv("Employee.csv")
print("data.head():")
data.head()

print("data.info():")
data.info()

print("isnull() and sum():")
data.isnull().sum()

print("data value counts():")
data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
print("data.head() for Salary:")
data["salary"]=le.fit_transform(data["salary"])
data.head()

print("x.head():")
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident"]]
x.head()

y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print("Accuracy value:")
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

print("Data Prediction:")
dt.predict([[0.5,0.8,9,260,6,0]])

from sklearn.tree import plot_tree
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plot_tree(dt, feature_names=x.columns, class_names=['salary', 'left'], filled=True)
plt.show()
*/
```

## Output:
<img width="1562" height="287" alt="Screenshot 2026-05-18 155645" src="https://github.com/user-attachments/assets/c29f30d9-cfe6-45c2-bad6-90bec2c6daea" />

<img width="540" height="409" alt="Screenshot 2026-05-18 160505" src="https://github.com/user-attachments/assets/650c776d-8a3f-4d60-a256-18ce6cc90b9c" />

<img width="281" height="518" alt="Screenshot 2026-05-18 160616" src="https://github.com/user-attachments/assets/732cc7ad-ddd1-4f53-a32d-592cbfa68392" />

<img width="203" height="235" alt="Screenshot 2026-05-18 160726" src="https://github.com/user-attachments/assets/57d190f9-a8e2-4959-bf49-be869bda4d01" />

<img width="1575" height="278" alt="Screenshot 2026-05-18 160838" src="https://github.com/user-attachments/assets/f0d03f95-df07-412a-b234-876d5536ecf1" />

<img width="1088" height="271" alt="Screenshot 2026-05-18 160926" src="https://github.com/user-attachments/assets/b325b40c-533d-450c-a467-c76e01098e17" />

<img width="1663" height="90" alt="Screenshot 2026-05-18 161342" src="https://github.com/user-attachments/assets/b907e3da-325c-49f0-b27d-de2a0124ec32" />

<img width="831" height="616" alt="Screenshot 2026-05-18 161445" src="https://github.com/user-attachments/assets/edf8a65b-cb5f-4246-b96e-932fc4a64701" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
