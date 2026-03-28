## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>

### Step2
<br>

### Step3
<br>

### Step4
<br>

### Step5
<br>

## Program:
```
import matplotlib.pyplot as plt
import numpy as np
from sklearn import datasets, linear_model, metrics
from sklearn.model_selection import train_test_split

housing = datasets.fetch_california_housing()
X = housing.data
y = housing.target

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=1
)

reg = linear_model.LinearRegression()
reg.fit(X_train, y_train)

print('Coefficients: ', reg.coef_)
print('Variance score: {}'.format(reg.score(X_test, y_test)))

plt.style.use('fivethirtyeight')
plt.scatter(reg.predict(X_train),
            reg.predict(X_train) - y_train,
            color="green", s=10, label='Train data')

plt.scatter(reg.predict(X_test),
            reg.predict(X_test) - y_test,
            color="blue", s=10, label='Test data')

plt.hlines(y=0, xmin=0, xmax=5, linewidth=2)
plt.legend(loc='upper right')
plt.title('Residual Errors')
plt.show()
```
## Output:

<img width="806" height="659" alt="image" src="https://github.com/user-attachments/assets/42e645f7-3ce4-4fd9-bc0a-5d4eac1b741b" />


### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
