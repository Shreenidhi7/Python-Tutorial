
- In this section, we will continue understanding the control statements
- In the last lecture we looked at what is IF and how it can be used.
- In this lecture, we will look at the IF counterpart ELSE
- ELSE will be used with IF always
	- IF can be used without an ELSE
	- But ELSE cannot be used without IF
- Syntax of IF-ELSE
	- if condition:
		- block of code to be executed when the condition is True
	- else:
		- block of code to be executed when the condition if False
- The ELSE block will execute only if the IF condition FALSE

```
# Syntax of IF-ELSE  
#   - if condition:  
#      - block of code to be executed when the condition is True  
#   - else:  
#      - block of code to be executed when the condition if False  
  
age = float(input("What is your age? "))  
if age >= 18:  
    print("Congrats! You can cast your vote!")  
else:  
    print("A few more years before you can vote")  
  
print("Reset of the program")

Output Response -
What is your age? 20
Congrats! You can cast your vote!
Reset of the program

What is your age? 10
A few more years before you can vote
Reset of the program
```


---
---

```
######################  
# Write a program to print if a number (int) is odd or even  
# even - when number is divisible by 2 - if the reminder is zero  
# odd - when number is not divisible by 2 - if the reminder is non-zero  
  
num = int(input("Enter a integer number: "))  
if num % 2 == 0:  
    print(f"The number {num} is even")  
else:  
    print(f"The number {num} is odd")
    
Output Response -
Enter a integer number: 10
The number 10 is even

Enter a integer number: 9
The number 9 is odd
```

----
----

```
#######################  
# Write a logic to print if a number is negative or positive  
num = float(input("Enter a number: "))  
  
if num > 0:  
    print(f"The number {num} is positive")  
elif num < 0:  
    print(f"The number {num} is negative")  
else:  
    print(f"The number {num} is zero")
    
Output Response -
Enter a number: 0
The number 0.0 is zero

Enter a number: 10
The number 10.0 is positive

Enter a number: -10
The number -10.0 is negative
```

---
---
