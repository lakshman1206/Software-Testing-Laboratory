# Ex.No: 3 To check the number is prime or not and inspect for failures.
 
### DATE: 27-08-24                                                                           
### REGISTER NUMBER : 212221040168
### AIM: 
Write a python program to check the number is prime or not and inspect for failures.
 
### Algorithm:
1. Start the program.
2. Get the number to be checked from the user.
3. If the number is less than or equal to 1, return "Not Prime".
4. If the number is 2, return "Prime".
5. Start the iteration from 3, For each iteration:
6. If the number is divisible by the current iteration value, return "Not Prime".
7. If the number is not divisible by any value from 2 to the square root, return "Prime".
8. Stop the program.

### Program:

```
num = input("Enter a number: ")

if num.isnumeric():
    z = int(num)
    if z <= 1:
        print("Not a Prime Number")
    elif z == 2:
        print("Prime Number")
    else:
        flag = 1  
        for i in range(2, int(z**0.5) + 1):
            if z % i == 0:
                flag = 0
                break
        if flag == 1:
            print("Prime Number")
        else:
            print("Not a Prime Number")
else:
    if not num.isalnum():
            print("Reason to fail: Special characters are not allowed enter valid integer")
    else:
            print("Reason to fail: Alphabets are not allowed enter valid integer")

```










### Output:

![Screenshot 2024-10-08 134729](https://github.com/user-attachments/assets/49499ed9-af44-429f-af17-1a7cafc07ed0)




### Result:
Thus, the python program to check the number is prime or not is implemented and the output is verified successfully.
