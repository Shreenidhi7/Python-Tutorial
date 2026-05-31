
- In this lecture, we will start to understand what are functions.
- We have already seeing the different types of function
	- print function
		- It is used to print something
		- It can print a string, single and multiple values
			- print("Hello World")
			- var = 100
				- print(var)
			- print(10,20,30)
		- Print function basically displays the output
- Function can take some values and does something for us.
	- Function has a name with brackets and has one or more values and it performs a task for us.
- There are 3 types
	- Inbuilt or Built In Functions
		- These are the functions that we get when we install python
		- These are written by Python developers and when we install python we can use these functions
		- Python interpreter has number of functions and types built into it that are always available
			- https://docs.python.org/3/library/functions.html
		- We have already seen few of them
			- range, length, input, id, min, max etc...
	- Functions that cannot be used directly but needs to be imported before using it.
		- Random module
			- We import the module called random and to use the functions available from these module, we have use the random function
				- print(random.randint())
					- The function randInt() is present in the module called random and it called used only if we import the random module.
	- We can create a function of our own - These are called User Defined Functions
		- Functions that are created or defined by users.
			- Function can contain any number of statements that perform a particular task
		- Why do we need to create these functions?
			- Code Reusability
				- We can write the re-usable code in a block - the block we call it as a function and that function can be called N number of times we want
					- It means the logic will be written once and can be used anytime/anywhere in the program.
			- Example -
```
number = int(input("Enter a number: "))  
  
if number % 2 == 0:  
    print(f"{number} is an even number")  
else:  
    print(f"{number} is an odd number")
```

---

- Syntax - User Defined Functions  
- def function_name(arg1,arg2,...,argN):  
	- statement1
	- statement2
	- ...
	- statementN

Example -
```
# User-Defined Function  
  
"""  
Syntax - User Defined Functions  
def function_name(arg1,arg2,...,argN):  
    statement1    
    statement2    
    ...    
    statementN
"""  
  
def checkEvenOrOdd(number):  
    if number % 2 == 0:  
        print(f"{number} is an even number")  
    else:  
        print(f"{number} is an odd number")  
  
number = int(input("Enter a number: "))  
checkEvenOrOdd(number)

Output Response -
Enter a number: 2
2 is an even number
```


---
---
