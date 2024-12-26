# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

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
import chardet
file='spam.csv'
with open (file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
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
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Pugazhsozhan.A
RegisterNumber: 24000166 
*/
```

## Output:
![SVM For Spam Mail Detection](sam.png)
![Screenshot 2024-12-26 104638](https://github.com/user-attachments/assets/257f963b-99a1-42db-80fb-c99f3b4713bf)
![Screenshot 2024-12-26 104650](https://github.com/user-attachments/assets/6867bb0a-5f28-479a-87ec-425ba5643b42)
![Screenshot 2024-12-26 104702](https://github.com/user-attachments/assets/6d133de8-c000-41fc-8401-35ebb2477273)
![Screenshot 2024-12-26 104743](https://github.com/user-attachments/assets/2960bec3-56e3-4fdb-832e-204f40c85af3)
![Screenshot 2024-12-26 104753](https://github.com/user-attachments/assets/b185934d-051d-4bb5-ac2a-119b82174861)
![Screenshot 2024-12-26 104803](https://github.com/user-attachments/assets/5957d4af-ec1e-4714-8c96-3cb326b20366)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
