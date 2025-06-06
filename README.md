# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.import numpy module

2.Get input from the user for number of rows and add it by 1 for number of column

3.Using np.zeros() set the matrix as null matrix.

4.Using nested for loop find the ratio and perform the elementary row operations and find the final matrix.

5.print and end the program
## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by:JOTHI GANESH P

RegisterNumber: 212224240065


import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#black substitution 
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ") 



```

## Output:
![gaussian elimination]()

![Screenshot 2025-04-15 082547](https://github.com/user-attachments/assets/5cfe0c5f-e228-46b4-a9ca-1f9b51b0f124)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

