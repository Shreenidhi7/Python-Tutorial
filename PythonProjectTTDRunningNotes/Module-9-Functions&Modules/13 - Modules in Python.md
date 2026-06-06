
- This section, we will understand what are modules in python.
- In Python, a module is a file containing definitions and statements
	- In short, it contains mostly functions that are defined in Python
	- So basically any Python file having Python code in it with the extension of .py file is a module
	- .py file can have functions, statements, variables of its own.
	- A module can also contain executable code or runnable code in it.
- Why do we use modules in Python?
	- Similar types of task or functions can be made part of the single file so that it can be grouped together so that the code/project is easier to read.
		- This makes the code easier to understand and use.
		- It also makes the code logically organized.
- There are 2 types of modules in Python
	- Built-in modules
	- User-defined modules

1. Built-In Modules
	1. Python built-in modules are the modules which are available when we install Python in our system.
	2. There are several built-in modules in python which we can import and use.
	3. Example - 
		1. math module
		2. random module
		3. datetime module
		4. keyword module
	4. How to import a module?
		1. Simple way of importing a module
			1. Syntax => import module_name
		2. If we want to import a certain function from a module, lets say a random module have functions like choices, random, shuffle [import only few functions of the module(not the whole module)]
			1. Syntax => from module_name import f1,f2,f3
	5. Example-
		1. math is a built-in module that can be imported directly using the import in my file
			1. so if i have to use any function of math module, 1st i have to import it and then use it => module_name.function_name(arguement)

- One way of importing modules
	- Direct way
```
# .py file is a module  
# Built-In Modules  
## math, random, datetime, ....  
  
# how to import a module in python  
# syntax - import module_name  
# syntax for importing only few function/variables -> from module_name import f1, f2, f3
# syntax to create an alias for the module that is imported: import module_name as alias_name
  
# calculate square root of the number  
import math  
num = 100  
output = math.sqrt(num)  
print(f"Square root of the {num} is {output}")  
print()  
  
# calculate the area of the circle  
import math  
radius = 2  
area_of_circle = math.pi * (radius ** 2)  
print(f"The value of pi is {math.pi}")  
print(f"Area of the circle with radius {radius} is: {area_of_circle}")

Output Response -
Square root of the 100 is 10.0

The value of pi is 3.141592653589793
Area of the circle with radius 2 is: 12.566370614359172
```

---

- Another way of importing modules
	- Only certain function from a module
	- Example - throw a dice
		- from random import radint
		- value = randint(1, 10)
	- Here if we observe we are not using the random function to import randint
		- random.randint(1,10)
			- when we import the full module, we have to use the module_name.function_name(argument)
	- Here we are directly calling randint(1,10)
		- if we write random.randint(1,10), then we will get an error -> it says its not defined.

```
# throw a dice/die  
## we need to generate a random value  
from random import randint  
value = randint(0, 6)  
print(f"The random value is: {value}")

Output Response -
The random value is: 4
```

---

- We can import a module and provide an alias to it.
	- There is another way and a syntax to create an alias for the module that is imported.
	- Syntax => import module_name as alias_name

```
# alias  
import datetime as dt  
print(f"current time {dt.time(hour=23, minute=15, second=35)}")  
print(f"current date and time {dt.datetime.now()}")

Output Response -
current time 23:15:35
current date and time 2026-06-06 23:15:34.090846
```

---
---
