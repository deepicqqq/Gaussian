## NAME: DEEPIKA P
## REGISTER NO: 212223240024
# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

​1. Start the program.

2. Enter the augmented matrix, which includes both the coefficients of the variables and the constants from the equations.

3. Count the number of equations (rows in the matrix).

4. Use forward elimination to make the entries below the main diagonal zero:

      For each row, eliminate the values below the current pivot by adjusting the rows beneath it.

5. Create an empty list (or array) for the solution and fill it with zeros.

6. Perform back substitution:

      Start from the last row and calculate the value of each variable one by one, moving upward.

7. Display the solution values.

8. End the program.

## Program:

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

