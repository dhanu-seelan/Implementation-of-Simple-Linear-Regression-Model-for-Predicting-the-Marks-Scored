# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Initialize and Prepare Data
Import required libraries and define input (X) and output (Y) datasets.
2.Create and Train Model
Initialize Linear Regression model and fit it using X and Y.
3.Obtain Model Parameters
Extract slope (m) and intercept (b) of the regression line.
Make Prediction
4.Take user input and predict output using the trained model.
5.Visualize Results
Plot actual data points and regression line using a graph.


## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: 
RegisterNumber:  212225040053
*/
```import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression



X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])


model = LinearRegression()


model.fit(X, Y)


m = model.coef_[0]
b = model.intercept_

print("Slope:", m)
print("Intercept:", b)


x_input = float(input("Number of hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])


Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
<img width="935" height="689" alt="image" src="https://github.com/user-attachments/assets/5f1cbb36-1137-455a-85b8-db6dc2dd64f9" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
