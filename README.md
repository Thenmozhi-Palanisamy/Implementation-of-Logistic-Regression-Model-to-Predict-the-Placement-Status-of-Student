# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: 
RegisterNumber:  
*/
```
import pandas as pd
data=pd.read_csv('Placement_Data.csv')
data.head()


data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis = 1)#removes the specified row or column
data1.head()


data1.isnull().sum()


data1.duplicated().sum()


from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"] = le.fit_transform(data1["gender"])
data1["ssc_b"] = le.fit_transform(data1["ssc_b"])
data1["hsc_b"] = le.fit_transform(data1["hsc_b"])
data1["hsc_s"] = le.fit_transform(data1["hsc_s"])
data1["degree_t"] = le.fit_transform(data1["degree_t"])
data1["workex"] = le.fit_transform(data1["workex"])
data1["specialisation"] = le.fit_transform(data1["specialisation"])
data1["status"] = le.fit_transform(data1["status"])
data1


x=data1.iloc[:,:-1]
x


y=data1["status"]
y


from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size = 0.2,random_state = 0)


from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(solver = "liblinear")# a library for large
lr.fit(x_train,y_train)
y_pred = lr.predict(x_test)
y_pred
*/

## Output:
![image](https://user-images.githubusercontent.com/95198708/232792645-c94ea977-7f7f-42f1-8bc2-2ef1eb21b069.png)
![image](https://user-images.githubusercontent.com/95198708/232792678-0f8793c5-41a6-4b44-b7ea-0d4548fa6158.png)
![image](https://user-images.githubusercontent.com/95198708/232792707-52d4ecaf-4576-4336-aeab-33b9d27d09d7.png)
![image](https://user-images.githubusercontent.com/95198708/232792751-21adfec8-6583-498f-9961-e0b4458638db.png)
![image](https://user-images.githubusercontent.com/95198708/232792799-9da1760e-c6cf-467f-b9d0-20997a32ae33.png)
![image](https://user-images.githubusercontent.com/95198708/232792844-58e72f49-24d1-46d9-9f42-43713101f033.png)




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
