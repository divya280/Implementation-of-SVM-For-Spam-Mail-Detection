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

![image](https://github.com/divya280/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/3eb81991-31a9-4d3d-af49-7ce1c7e8932a)

### data.info()

![image](https://github.com/divya280/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/50bf1615-cca7-428a-9155-b31d2f22b808)

### data.isnull()

![image](https://github.com/divya280/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/562a1101-f680-423b-a4d8-25983411b10f)

### y_pred:

![image](https://github.com/divya280/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/b7197d9b-4ce1-49d6-80e3-efd910ecf8cf)

### Accuracy:

![image](https://github.com/divya280/Implementation-of-SVM-For-Spam-Mail-Detection/assets/82276099/79dde9a7-b6e4-4d81-9b13-fc5ad5b17868)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
