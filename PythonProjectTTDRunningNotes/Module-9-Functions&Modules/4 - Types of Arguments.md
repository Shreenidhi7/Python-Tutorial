
- In this section, we will learn about types of arguments that we can have in Python functions.

1. Positional Arguments
	1. Positional Arguments are nothing but when we pass the arguments in the order of their position.
		1. Position Arguments - Passing the arguments in order of their position
			1. Here the 1st value goes to the  1st argument and the 2nd value goes to the 2nd argument
			2. The arguments gets their value with their position
				1. a gets 1
				2. b gets 2
```
# Positional Argument - Passing the arguments in order of their position  
def add(a, b):  
    return a + b  
  
result = add(1, 2)

Output Response -
3
```

---

2. Default Arguments
	1. We can assign Default values to 1 or more arguments and when we do that, we are creating something called as an Optional Arguments
		1. It means that we don't need to pass a value for an argument that we making as Default
		2. In the function definition, we can make an arguement value to be default, which means the user or anyone who is calling this function need not have to pass the value. The default value of 10 will be taken
		3. If we pass the value, then the value will be considered, but if we don't pass the value, then the default value will be considered.
		4. In the 2nd example below, 
			1. a is the positional argument, so 1 is considered at a
			2. we don't have any value that is passed at b, so the default value defined at the function definition level i.e b=10 will be considered.
		5. When we create a default argument, that argument becomes optional to pass while calling the function
```
Example - 1
# Default Argument  
def add(a, b=10):  
    print(f"a : {a}, b : {b}")  
    return a + b  
result = add(1, 2)  
print(result)

Output Response -
a : 1, b : 2
3

----------------
Example - 2
# Default Argument  
def add(a, b=10):  
    print(f"a : {a}, b : {b}")  
    return a + b  
result = add(1)  
print(result)

Output Response -
a : 1, b : 10
11
```

- In the previous case of positional argument, when we don't have the argument declared as Default.
- Also if we don't pass the value while calling the function
- In that case, we will get an error
- In case of positional arguments, when there is no default value - a and b both are positional arguments and we need values for both of them.

```
# Positional Argument - Passing the arguments in order of their position  
def add(a, b):  
    return a + b  
result = add(1)  
print(result)

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\9-Functions & Modules\4-TypesOfArguments.py", line 4, in <module>
    result = add(1)
TypeError: add() missing 1 required positional argument: 'b'
```

---

Another Example of Default
- Important - The non-default argument should NOT follow the default argument

```
def add(a, b=10, c):  
    print(f" a: {a} , b: {b} , c: {c}")  
    return a + b + c  
  
result = add(10, 20, 30)  
print(result)

Output Response -
File "D:\Python\PythonTTDTutorial\9-Functions & Modules\4-TypesOfArguments.py", line 16
    def add(a, b=10, c):
                     ^
SyntaxError: parameter without a default follows parameter with a default
```

- In simple words, there shouldn't be any regular positional parameter after the Default parameter.
	- [Positional Arguments cannot come after Default Argument]
		- It is not allowed in Python

```
def add(a, b, c=10):  
    print(f"a: {a} , b: {b} , c: {c}")  
    return a + b + c  
  
result = add(10, 20, 30)  
print(result)  
  
result1 = add(10, 20)  
print(result1)

Output Response -
a: 10 , b: 20 , c: 30
60
a: 10 , b: 20 , c: 10
40
```

---

- Now, what if we want to only 1st and 3rd arguments
- Lets say we have a function which has B and C as defaults, so B & C are 2 optional parameter while calling the function.
```
def add(a, b=10, c=10):  
    print(f"a: {a}, b: {b}, c: {c}")  
    return a + b + c  
  
result = add(10, 20, 30)  
print(result)

Output Response -
a: 10, b: 20, c: 30
60
```

- There is a way to give value of A and C, and skip B
- We need to use something called "keyword" argument or "named" argument
	- We need to specify the argument during the function call
		- add(10, c=50)
	- here 10 will go to A and we are specifying 50 to go to C and B will take default value
```
def add(a, b=10, c=10):  
    print(f"a: {a}, b: {b}, c: {c}")  
    return a + b + c  
  
result = add(10,c=50)  
print(result)

Output Response -
a: 10, b: 10, c: 50
70
```

- This keyword value can be used across any argument
	- add(a=10,c=50,b=20)
- In this case, we are not passing the values by argument order but using the key argument.

---
---

- Positional Arguments - Takes the value with the position, with respect to the position
- Default Arguments - It has default value (its an optional argument)
- Keyword Arguments - We use the argument name while calling the function

---
---

