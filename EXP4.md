# Ex.No: 4 check the given number is Armstrong number or not and inspect for failures.
### DATE:                                                                            
### REGISTER NUMBER : 212221040168
### AIM: 
Write a python program to check the number is Armstrong number or not and inspect for failures.

### Algorithm:
1.  Start the program.
2.	Read an integer input number.
3.	Initialize the variables current_digit, sum = 0, and num = number.
4.	Repeat Steps 5 to 7 until num > 0
5.	current_digit = (num % 10).
6.	sum = sum + (current_digit * current_digit * current_digit). 7. Stop the program.
7.	num = num / 10.
8.	Check if sum == number. If true, print "It is an Armstrong Number." Otherwise, print "It is not an Armstrong Number."
9.	Stop the program.

### Program:


```
x = input("Enter the input: ")
if x.isnumeric():
    x = int(x)
    temp = x
    cube = 0
    while temp > 0:
        digit = temp % 10
        cube += digit ** 3
        temp //= 10
    
    if cube == x:
        print("Armstrong Number")
    else:
        print("Not Armstrong Number")
else:
    if not x.isalnum():
            print("Reason to fail: Special characters are not allowed enter valid integer")
    else:
            print("Reason to fail: Alphabets are not allowed enter valid integer")

```










### Output:
![Screenshot 2024-10-08 135429](https://github.com/user-attachments/assets/88b3fc9a-b3be-48d7-8682-18428ff3ccba)






### Result:
Thus, the python program to check the number is Armstrong number or not implemented and the output is verified successfully.


