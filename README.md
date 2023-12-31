# Exp-09-Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
<br/>
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

## Program:
```
# Univariate Linear Regression
# Developed by: P.LOKNAATH
# Register Number : 212223240080

import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean=np.mean(x)
ymean=np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color="Red")
plt.plot(x,ypred,color="Blue")
plt.show()

```

## Output
![code](https://github.com/Loknaath-sec/Univariate-Linear-Regression/assets/145742558/bdee407e-f84c-44ba-a215-b20571887edb)
<br/>
![image](https://github.com/Loknaath-sec/Univariate-Linear-Regression/assets/145742558/4b19b7e7-024c-4215-a20d-7c250167b133)
<br/>

![9(a)](https://github.com/Loknaath-sec/Univariate-Linear-Regression/assets/145742558/cd82c7dd-c78e-450d-9c4a-69ad9ddc1ef7)
</br>
![9(b)](https://github.com/Loknaath-sec/Univariate-Linear-Regression/assets/145742558/6aebb5c4-5f0e-4a23-808a-9992100463c1)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
