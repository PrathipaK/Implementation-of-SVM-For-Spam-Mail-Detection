# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## EQUIPMENT'S REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## ALGORITHM:
1. Import the required packages.
2. Import the dataset to operate on.
3. Split the dataset.
4. Predict the required output.
5. End the program.

## PROGRAM:
```python
Program to implement the SVM For Spam Mail Detection..
Developed by: Prathipa K
RegisterNumber: 212219040111

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

## OUTPUT:
### Data Head:
![output](/images/head.png)

### Data Info:
![output](/images/info.png)

### Data isnull():
![output](/images/isnull.png)

### y_pred:
![output](/images/ypred.png)

### Accuracy:
![output](/images/accracy.png)


## RESULT:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.