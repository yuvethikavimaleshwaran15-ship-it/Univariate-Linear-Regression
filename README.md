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

#Developed by : Yuvethika V 
#Regiister num:26016105
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
</br><img width="667" height="585" alt="Screenshot 2026-11-24 113748" src="https://github.com/user-attachments/assets/859acd83-3e61-48c4-ac2c-30d1bac86980" />

</br><img width="761" height="602" alt="Screenshot 2026-11-24 113807" src="https://github.com/user-attachments/assets/65a17cde-a819-4493-b839-346fb5fcf491" />

</br><img width="788" height="545" alt="Screenshot 2026-11-24 113821" src="https://github.com/user-attachments/assets/a44ccda4-38e3-4e3e-992c-c10477a00bd7" />

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
