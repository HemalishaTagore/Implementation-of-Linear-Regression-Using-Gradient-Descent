# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:

## Developed by: HEMALISHA T
## RegisterNumber: 212225040123

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data = pd.read_csv("50_startups.csv")
print(data.head())
X = data['R&D Spend'].values
y = data['Profit'].values
X = (X - X.mean()) / X.std()
y = (y - y.mean()) / y.std()
m = 0
c = 0
L = 0.01
epochs = 1000
n = len(X)
for i in range(epochs):
    y_pred = m * X + c
    D_m = (-2/n) * sum(X * (y - y_pred))
    D_c = (-2/n) * sum(y - y_pred)
    m = m - L * D_m
    c = c - L * D_c
print("Slope (m):", m)
print("Intercept (c):", c)
y_pred = m * X + c
plt.scatter(X, y, color='blue')
plt.plot(X, y_pred, color='red')
plt.xlabel("R&D Spend")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.show()
```

## Output:
![linear regression using gradient descent](.png)


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
