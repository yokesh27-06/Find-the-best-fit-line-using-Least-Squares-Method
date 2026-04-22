# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: YOKESH H  
RegisterNumber: 212224230312
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array([1,2,3,4,5])
Y=np.array([2,4,5,4,5])
x_mean=np.mean(X)
y_mean=np.mean(Y)
numerator=np.sum((X-x_mean)*(Y-y_mean))
denominator=np.sum((X-x_mean)**2)
m=numerator/denominator
b=y_mean-m*x_mean
print("Slope(m):",m)
print("Intercept(b):",b)
Y_pred=m*X+b
x=input("Enter value:")
yy = m * float(x) + b
print("Value:", yy)
plt.scatter(X, Y, label="Data Points")
plt.plot(X, Y_pred, label="Best Fit Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.title("Univariate Linear Regression")
plt.show()
```
## Output:
<img width="818" height="658" alt="Screenshot 2026-04-22 093805" src="https://github.com/user-attachments/assets/771e7abe-eb27-4e49-87ae-e4557892f7e1" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
