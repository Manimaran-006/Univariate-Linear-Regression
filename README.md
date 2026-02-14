# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Preprocessing input data
import numpy as np
import matplotlib.pyplot as plt
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(X,Y)
plt.show()

#Building the model

X_mean=np.array(X)
Y_mean=np.array(Y)

num = 0
den = 0
for i in range(len(X)):
    num += (X[i] - X_mean)*(Y[i] - Y_mean)
    den += (X[i] - X_mean)**2

m = num/den
c = Y_mean - m*X_mean

print(m, c)

#Making predications

Y_pred = m*X+c
print(Y_pred)

plt.scatter(X,Y)
plt.plot([min(X), max(X)],[min(Y_pred), max(Y_pred)],color='red')
plt.show()
```
## Output

<img width="812" height="737" alt="image" src="https://github.com/user-attachments/assets/e2005e43-cbf6-42cf-a32b-0559d2f5e6be" />
<img width="1111" height="450" alt="image" src="https://github.com/user-attachments/assets/b332c345-7b16-413b-937e-724cd86bdcbc" />
<img width="857" height="750" alt="image" src="https://github.com/user-attachments/assets/7b6a2a74-7e59-447d-9bc6-2a2d20193fd9" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
