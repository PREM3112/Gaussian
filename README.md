# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable. 
2. For gaussian elimination method, we want to make 2nd and 3rd column zero.
3. For that we want to make a range accorting to our program output.
4. Then print the program with correct form then the output will display.


## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: PREM.R
RegisterNumber: 23002486
*/
import numpy as np
n = int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,res[i]),end= " ")
    
```

## Output:
![gaussian elimination]()
![Screenshot 2023-12-25 191951](https://github.com/PREM3112/Gaussian/assets/145449383/1d3354db-89b5-4926-8714-c305c9fe8b2d)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

