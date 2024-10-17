# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
## Step 1 :
Import the necessary python packages using import statements.

## Step 2 :
Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

## Step 3 :
Split the dataset using train_test_split.

## Step 4 :
Calculate Y_Pred and accuracy.

## Step 5 :
Print all the outputs.

## Step 6 :
End the Program.

## Program:
Program to implement the SVM For Spam Mail Detection..
## Developed by: VINODINI R
## RegisterNumber: 212223040244

```python
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

data.head()

data.info()

data.isnull().sum()

x=data["EmailText"].values
y=data["Label"].values

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



## Output:
## DATA.HEAD() :

![ml-9 1](https://github.com/jagadeeshreddy561/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120623104/57a7de43-13ee-4f3a-bb26-067bc84d2cbf)


## DATA.INFO() :


![ml-9 2](https://github.com/jagadeeshreddy561/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120623104/0d4bf0f6-316b-4aa3-962d-6e6a96c7f484)


## DATA.ISNULL().SUM() :


![ml-9 3](https://github.com/jagadeeshreddy561/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120623104/52d49705-8cfc-466f-aa36-0956e1377aca)


## Y_PRED :

![ml-9 4](https://github.com/jagadeeshreddy561/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120623104/43d12187-df10-440c-9834-372efe50f9ef)


## ACCURACY :

![ml-9 5](https://github.com/jagadeeshreddy561/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120623104/60b6de18-8e8d-4a40-9255-4ab98b87faa0)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
