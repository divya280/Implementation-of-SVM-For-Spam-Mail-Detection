# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages
2. Import the dataset to operate on
3. Split the dataset
4. Predict the required output
5. End the program

## Program:
/*
### Program to implement the SVM For Spam Mail Detection..
### Developed by: V.Divyashree
### RegisterNumber:  212223230051
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
*/


## Output:
### data.head()
![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/e3ed663b-35ed-41a1-b43e-5bc3ed8ce011)

### data.info()

![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/96670ee1-e73f-4687-ac80-9ff7bbca09ec)

### data.isnull()

![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/cca8de81-b3a9-4565-8119-9810814b8587)

### y_pred:

![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/0bbcf87c-ca7b-47a2-8ced-6bec91c5881c)

### Accuracy:

![image](https://github.com/AkilaMohan/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/68006693-d0f8-4614-bf22-2efbac5afbf0)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
