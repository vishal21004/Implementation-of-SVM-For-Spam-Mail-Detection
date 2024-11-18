# EX 11: Implementation-of-SVM-For-Spam-Mail-Detection
### Date : 11/11/24
## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1.Import the necessary python packages using import statements.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Split the dataset using train_test_split.

4.Calculate Y_Pred and accuracy.

5.Print all the outputs.

6.End the Program.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: VISHAL M.A
RegisterNumber: 212222230177

import chardet 
file='spam.csv'
with open(file, 'rb') as rawdata: 
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd
data = pd.read_csv("spam.csv",encoding="Windows-1252")
data.head()
data.info()
data.isnull().sum()

X = data["v1"].values
Y = data["v2"].values
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test = train_test_split(X,Y,test_size=0.2, random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
X_train = cv.fit_transform(X_train)
X_test = cv.transform(X_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(X_train,Y_train)
Y_pred = svc.predict(X_test)
print("Y_prediction Value: ",Y_pred)

from sklearn import metrics
accuracy=metrics.accuracy_score(Y_test,Y_pred)
accuracy
*/
```

## Output:

### Result Output

![img 1](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/6cd93a22-2959-4e43-a424-1a25103785d0)


### data.head()
![img2](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/0f89936d-4669-44b5-9b1f-90ac1a1d38f2)



### data.info()
![img 3](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/46803d91-3059-48e7-98bb-2d82fb552998)



### data.isnull().sum()
![img 4](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/7ebe7023-84e7-4ddc-9104-90313eab62f9)
![img5](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/99cec0d4-819f-4c4a-a382-d7ae1f25eafe)



### Y_prediction Value
![prediction value](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/068d6e50-980d-4ff5-9971-d19414162271)



### Accuracy Value
![last vaue](https://github.com/vishal21004/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119560110/be259d7a-7fed-4505-bd97-b43118b96c75)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
