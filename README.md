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
Developed by: DEEPIKA.U
RegisterNumber:  212225040060
*/

import numpy as np
import matplotlib.pyplot as plt
x=np.array([1,2,3,4,5])
y=np.array([2,4,5,4,5])
x_mean=np.mean(x)
y_mean=np.mean(y)
nume=np.sum((x-x_mean)*(y-y_mean))
den=np.sum((x-x_mean)**2)
m=nume/den
b=y_mean-m*x_mean
print("slope (m):",m)
print("intercept (b):",b)
y_pred = m * x + b
print(y_pred)
plt.scatter(x, y, label="Data")
plt.plot(x, y_pred, label="Regression Line")
plt.legend()
plt.show()
```

## Output:

<img width="556" height="439" alt="image" src="https://github.com/user-attachments/assets/fca126b9-5bc5-4fa3-b8b0-44ee6447fa88" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
