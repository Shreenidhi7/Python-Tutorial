
- This section, we shall look at Docstrings and functions in python.
- We can use documents or docstrings inside our function definition so that anybody who sees our function can understand what is done inside the function.
- So, docstrings are a good thing to be written inside the function so that we can describe the arguments, what are those arguments, what is expected return value, what is going to happen inside the function

- The docstring should be the 1st function that is written inside the function definition
- It is written in Triple Quotes [""" """]
	- When we type """ and press Enter, it gives me a format in which i can write whatever we want and can return any value as well.
```
def func():  
    """  
    This is a docstring    We can write what the function does here    
    :return: None  
    """    
    return None  
  
func()

Output Response -

```

- Now, how do we know that the docstring is added to the function or not?
	- There is a function called help()
		- The help() function basically can give the details about any function
		- This will display what is exactly written as the docstring for the function
			- Without the print function as well, we can directly use the help function

```
def func():  
    """  
    This is a docstring    We can write what the function does here    
    :return: None  
    """    
    return None  
  
# func()  
print(help(func))

Output Response -
Help on function func in module __main__:

func()
    This is a docstring
    We can write what the function does here
    :return: None

None
```

--

```
def divide(num1, num2):  
    """  
    num1: A number to be divided [Numerator]    num2: A number that divides num1 [Denominator]    :return: float (if num2 is non-zero) OR str (if num2 is 0)  
    """    if num2 ==0:  
        return "Cannot divide as Denominator is 0"  
    else:  
        result = num1 / num2  
        return result  
  
help(divide)  
print(divide(10, 0))
print(divide(10, 2))

Output Response -
Help on function divide in module __main__:

divide(num1, num2)
    num1: A number to be divided [Numerator]
    num2: A number that divides num1 [Denominator]
    :return: float (if num2 is non-zero) OR str (if num2 is 0)

Cannot divide as Denominator is 0
5.0
```

- Help() function will automatically print the output of docstring.
- Anything that we think that should be conveyed as a message or an explanation or a documentation of your function can be written in docstings
- Also important thing - it should be written as the 1st thing in the function definition.
	- If its not used as the 1st thing in the function definition, then in the output it will not show the documentation.
- It should be the 1st thing in the function - its a rule.

----

- We learnt how to create docstrings and how to use help function to know the information about the function
- We have used help() on the user-defined function,but it can be used on built-in functions aswell
	- example - help(len)

---
---
