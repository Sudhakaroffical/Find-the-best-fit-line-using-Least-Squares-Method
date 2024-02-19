# Implementation of Univariate Linear Regression
### AIM:  
To implement univariate Linear Regression to fit a straight line using least squares. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE:**
### Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook
### Algorithm:
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula.<img width=30% height=7% alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

<table>
<tr>
<td valign='top'>

### Program:
```Python
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
Nume,Deno=0,0
for i in range(len(X)):
    Nume+=(X[i]-Xmean)*(Y[i]-Ymean)
    Deno+=(X[i]-Xmean)**2
M=Nume/Deno
C=Ymean-(M*Xmean)
print("Slope : ",M)
print("Y-intercept : ",C)
Ypred=(M*X)+C
print("Predicted Values :",Ypred)
plt.scatter(X,Y)
plt.plot(X,Ypred)
plt.show()
```
Developed By: **SUDHAKAR K** <br>
Register No: **212222240107**
</td> 
<td>
  
### Output:
Slope : 1.537302371541502  
Y-intercept: 2.8370580808080827  
Predicted Values: [ 8.37134662 10.21610946 13.90563516 13.44444444 19.28619346 12.21460255
 14.98174682 17.44143061 11.13849089]

![sudhakar ml 1](https://github.com/Sudhakaroffical/Find-the-best-fit-line-using-Least-Squares-Method/assets/118622513/8c83f33f-111c-447e-bb0d-01c026ee02a0)

</td>
</tr> 
</table>

### Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
