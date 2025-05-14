# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the necessary library (NumPy).

2. Accept or define the augmented matrix representing the system of linear equations.

3. Perform row operations to convert the matrix into an upper triangular form.

4. Use back substitution to find the solutions of the variables.

 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: DEEPIKA P
RegisterNumber: 2122233240024
*/
```
import numpy as np\
a = np.array([[2, 1, -1, 8],\
              [-3, -1, 2, -11],\
              [-2, 1, 2, -3]], dtype=float)\

n = len(a)\
for i in range(n):\
    for j in range(i+1, n):\
        ratio = a[j][i] / a[i][i]\
        a[j] = a[j] - ratio * a[i]\
x = np.zeros(n)\
x[n-1] = a[n-1][n] / a[n-1][n-1]\

for i in range(n-2, -1, -1):\
    x[i] = a[i][n]\
    for j in range(i+1, n):\
        x[i] -= a[i][j] * x[j]
    x[i] = x[i] / a[i][i]
print("The solution is:", x)


## Output:

![image](https://github.com/user-attachments/assets/8bfbc970-d8f7-4b21-8ece-3b0b1bd90b46)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

