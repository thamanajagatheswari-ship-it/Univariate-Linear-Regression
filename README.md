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
#Name :  Thamana G
#Reg no: 26018758
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
</br>
<img width="716" height="590" alt="Screenshot 2026-11-24 113738" src="https://github.com/user-attachments/assets/19a45a67-7ed9-4ff2-9c6a-2f3796d80580" />

</br>
<img width="761" height="615" alt="Screenshot 2026-11-24 113754" src="https://github.com/user-attachments/assets/6c061790-4cf5-4c7b-9c57-4833c35de028" />

</br>
<img width="702" height="531" alt="Screenshot 2026-11-24 113805" src="https://github.com/user-attachments/assets/0fca2a8b-4fc4-4d6c-843a-eb991c9a2a8d" />

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
