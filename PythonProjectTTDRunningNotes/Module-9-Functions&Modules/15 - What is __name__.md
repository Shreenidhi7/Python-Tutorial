
- In the last lecture, we looked at how to create a user-defined module.
- We created a module called arithmetic.py and a couple of functions in it.
- And we created a file UserDefinedModule and imported the whole arithmetic module as well as the specific functions of the module [arithmetic]
- Lets take an example and try to understand the concept of [__name__] / [ __variable__]

- What is the need of [ __name__ variable] ?
	- If a module is written, it can be imported, but if we want to execute the module as a runnable code

- Module File
```
def add(num1, num2):  
    return num1 + num2  
  
def square_root(num):  
    return num ** 0.5  
  
a = 10  
b = 20  
result = add(a, b)  
print(f"Addition of {a} and {b} is {result}")

Output Response -
Addition of 10 and 20 is 30
```

- Regular .py file
```
import ArithmeticModule2  
  
a = 100  
out = ArithmeticModule2.square_root(a)  
print(f"Square_root of {a} is {out}")

Output Response -
Addition of 10 and 20 is 30
Square_root of 100 is 10.0
```

- If we observe the response of the Regular .py file, we see 2 outputs.
	- One output is from the Module file
	- Another output is from the Regular .py file
- Why is it getting printed even though we are not calling it manually or purposefully, we are just importing and using/calling the squareroot function.
	- The way Python modules work is that when we import a python module and if there is a runnable code or executable code in that file, that code will also gets executed while import.
		- This is because when we are importing the module, the functions in the modules should be executed to put them in the memory, so that we can use them.
		- This ArithmeticModule2.py executable code or runnable code gets executed while we import the module
	- So what do we want is when i am importing a module, i don't want the executable code to run from the module file, i just want them to be run when i call those functions from a regular .py file.
		- In this kind of scenario, we use this variable called [ __name__]
			- This is a special variable in python that helps us to write an executable code inside our module
			- [ __name__ ] => Its called Dunder Name
				- Its a special variable which is pre-defined in python
				- It will have a value set to the module name
```
ArithmeticModule2.py

def add(num1, num2):  
    return num1 + num2  
  
def square_root(num):  
    return num ** 0.5  
  
print(f"__name__ value in arithmetic module is {__name__}")

if __name__ == "__main__":  
    a = 10  
    b = 20  
    result = add(a, b)  
    print(f"Addition of {a} and {b} is {result}")
    
Output Response -
__name__ value in arithmetic module is __main__
30
```

- Regular .py function
```
import ArithmeticModule2  
  
a = 100  
out = ArithmeticModule2.square_root(a)  
print(f"Square_root of {a} is {out}")

Output Response -
Square_root of 100 is 10.0
```


---
---

