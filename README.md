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
Developed by: **HITHESH RAJ R K**
RegisterNumber: **212225040129**
*/

import numpy as np
import matplotlib.pyplot as plt

x=np.array([1,2,3,4,5])
y=np.array([2,4,5,4,5])
n=len(x)

m=((n* np.sum(x*y) )-(np.sum(x) * np.sum(y))) / ((n * np.sum(x**2)) - (np.sum(x) ** 2))
c=(np.sum(y) - m * np.sum(x)) / n

print(f"Slope: {m}")
print(f"Intercept: {c}")

y_predicted=m*x+c

print(y_predicted)

inp=float(input("Enter input value: "))
out=m*inp+c
print(f"Output value: {out}")
          
          
plt.scatter(x,y,color='blue',label='actual value')
plt.plot(x,y_predicted,color='red',label='plotted line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression using Least Square Method')
plt.legend()
plt.show()

```

## Output:

<img width="827" height="705" alt="Screenshot 2026-04-26 200419" src="https://github.com/user-attachments/assets/101f9c3d-041e-4c73-a5b0-f503959408d2" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
