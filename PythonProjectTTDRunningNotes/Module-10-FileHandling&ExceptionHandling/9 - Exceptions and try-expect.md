
- Till now, we have been seeing a lot of errors in Python that we encounter and we try to fix them
	- Syntax error, Name error, Value error, Index error, EndofFile error, FileNotFound error etc..

- Lets try to classify errors in python in this section.
- We shall understand what are exceptions and how to handle them in a basic level.
- There are 2 classification of errors that we see in Python
	1. Compile Time Error
		- Syntax Error
			- If there is issue with syntax, we get the syntax error
		- Indentation Error
			- If we don't provide the right indentation, then we encounter an indentation error

```
# Syntax Error  
age = 24  
print(age

Output Response -
    print(age
         ^
SyntaxError: '(' was never closed
```

```
## Indentation Error  
age = 24  
if age >= 18:  
print(age)

Output Response -
    print(age)
    ^^^^^
IndentationError: expected an indented block after 'if' statement on line 13
```

2. Exceptions
	1. While executing the program, errors can be detected.
		1. There are called Exceptions [Errors during Execution]
		2. Built-In Exceptions
			1. These are the errors or exceptions in python when there is an issue with the program and python identifies that issue and gives it to us.

```
## Exceptions  
print(10/0)

x = 100  
result = x+y

Output Response -
    print(10/0)
          ~~^~
ZeroDivisionError: division by zero

    result = x+y
               ^
NameError: name 'y' is not defined
```


---

- How to handle these error and exceptions
	- To handle them we can use something called Try and Except blocks
		- When any of these error happens the python stops execution.
		- It stops the python project and stops the execution going ahead
			- The execution doesn't proceed.

- When we are writing some application or writing some program, we shouldn't abruptly terminate the program because of these errors.
- We need to anticipate these kind of errors and handle them gracefully

- We will learn how we can use these Try-Except blocks statements to handle exceptions in Python.

```
num1 = int(input("Enter a number: "))  
num2 = int(input("Enter another number: "))  
  
try:  
    result = num1 / num2  
    print(result)  
except:  
    print("The denominator cannot be equal to zero")
    
try:  
    result = num1 / num2  
    print(result)  
except ZeroDivisionError:  
    print("The denominator cannot be equal to zero")
    
Output Response -
Enter a number: 10
Enter another number: 0
The denominator cannot be equal to zero
```

---

- Handling multiple exceptions

```
try:  
    num1 = int(input("Enter a number: "))  
    num2 = int(input("Enter another number: "))  
    result = num1 / num2  
    print(result)  
except ValueError:  
    print("Invalid input")  
except ZeroDivisionError:  
    print("The denominator is zero")
    
Output Response -
Enter a number: 10
Enter another number: d
Invalid input

Enter a number: 10
Enter another number: 0
The denominator is zero
```

- If there is no exception handling, then the program will not end gracefully.
	- It will end abruptly.

---
---
