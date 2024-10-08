# Ex.No: 2   Matrix Multiplication 

### DATE:                                                                            
### REGISTER NUMBER : 212221040168

### AIM: 
Write a python program for matrix multiplication and inspect for failures.
 
### Algorithm:

Algorithm:
1. Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program.
### Program:

```
r1, c1 = input("enter row and column count in matrix 1: ").split()
r2, c2 = input("enter row and column count in matrix 2: ").split()
if r1.isnumeric() and c1.isnumeric() and r2.isnumeric() and c2.isnumeric():
    r1 = int(r1)
    c1 = int(c1)
    r2 = int(r2)
    c2 = int(c2)
    if c1 != r2:
        print("Matrix multiplication not possible.\nReason to fail: Number of columns in matrix 1 must be equal to number of rows in matrix 2.")
    elif max(r1, c1, r2, c2) > 20 or min(r1, c1, r2, c2) == 0:
        print("Matrix multiplication not possible. \nReason to fail: size of buffer will be not be sufficient to handle this multiplication. ")
    else:
        matrix1 = []
        matrix2 = []
        
        print("Enter elements for matrix 1:")
        for i in range(r1):
            row = []
            for j in range(c1):
                row.append(int(input("Element [{}][{}]: ".format(i, j))))
            matrix1.append(row)
        
        print("Enter elements for matrix 2:")
        for i in range(r2):
            row = []
            for j in range(c2):
                row.append(int(input("Element [{}][{}]: ".format(i, j))))
            matrix2.append(row)
        
        result = [[0] * c2 for _ in range(r1)]
        
        for i in range(r1):
            for j in range(c2):
                sum = 0
                for k in range(c1):
                    sum += matrix1[i][k] * matrix2[k][j]
                result[i][j] = sum
        
        print("Resultant matrix:")
        for row in result:
            print(' '.join(map(str, row)))
else:
    if not r1.isalnum() or not c1.isalnum() or not r2.isalnum() or not c2.isalnum():
            print("Reason to fail: Special characters are not allowed enter valid integer")
    else:
            print("Reason to fail: Alphabets are not allowed enter valid integer")

```











### Output:

![Screenshot 2024-10-08 133725](https://github.com/user-attachments/assets/994ecc89-7f0f-4908-b0dd-622bd97ca559)





### Result:
Thus, the python program for matrix multiplication is implemented and the causes for its failure is introspected successfully.

