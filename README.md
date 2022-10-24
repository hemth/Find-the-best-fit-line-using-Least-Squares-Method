Implementation of Univariate Linear Regression
AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:HEMANTH KUMAR B 
RegisterNumber:212220040047
*/
import numpy as np
import matplotlib.pyplot as plt

#assign input

X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])

#mean values of input
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)

num=0
denum=0

for i in range(len(X)):
  num+=(X[i]-X)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

  #find m
  m=num/denum

  #find b
  b=Y_mean-m*X_mean
  print(m,b)

  #find Y_pred
  Y_pred=m*X+b
  print(Y_pred)

  #plot graph
  plt.scatter(X,Y)
  plt.plot(X,Y_pred,color='Blue')
  plt.show()


Output:
<img src="https://github.com/hemth/Find-the-best-fit-line-using-Least-Squares-Method/blob/main/196476074-cb966728-7e18-4f12-91c1-d273ae0ad587.png" alt="best-fit-line"/>


Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
