# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
First,we want to import numpy,then import sys,assume a variable.
For gaussian elimination method, we want to make 2nd and 3rd column zero.
For that we want to make a range accorting to our program output.
Then print the program with correct form then the output will display.

## Program:

/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Darshan V
RegisterNumber: 212224230050
*/
```
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero dectected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
```

## Output:
![Screenshot 2025-04-15 102633](https://github.com/user-attachments/assets/2f6f3f2a-a517-4725-b440-26e5527df3e0)
![Screenshot 2025-04-15 102647](https://github.com/user-attachments/assets/bf760bbd-d6e2-4351-9a9a-50108125bcde)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

