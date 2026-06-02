
- We shall continue to under "User-Defined" functions in Python
- In this section, we will look at how to return a value or multiple values from a function.

```
# Returning a Value from a function
def even_or_odd(num):  
    if num % 2 == 0:  
        print("Even")  
    else:  
        print("Odd")  
  
even_or_odd(5)

Output Response -
Odd
```

- In the above function, we are not returning a value, instead we are just printing a statement
- How to check that any function return something or not?
	- We can store the function call in a variable and print the result
		- result = even_odd(9)
		- print(result)
```
# Returning a Value from a function
def even_or_odd(num):  
    if num % 2 == 0:  
        print("Even")  
    else:  
        print("Odd")  
  
result = even_or_odd(5)  
print(result)

Output Response - 
Odd
None
```

- If we do that in the output we see, Odd and None both.
	- We we call a function and the function doesn't return anything, Python internally returns "None"
	- So if a function returns none, it gets stored in the result [whatever the function return, thats get stored in a variable called result]
			- Since the function doesn't return anything, Python returns "None" and that gets stored in the variable called result.
- Now, Instead of returning "None" or instead of printing "Odd/Even" , if we want these values to be returned out of the function then thats called the "Returning values from the function"
	- Instead of using print() in the even_or_odd function, we can use the return keyword and the value to be returned
		- Syntax - return value
			- retrun "Even"
			- return "Odd"
	- When we run this program, we don't get "Odd" and "None" both at the output instead we get only "Odd" at the output, this is because we are returning some value from the function and we are capturing the same at a variable and we are printing the variable

```
# Returning a Value from a function  
  
def even_or_odd(num):  
    if num % 2 == 0:  
        return "Even"  
    else:  
        return "Odd"  
  
result = even_or_odd(5)  
print(result)

Output Response -
Odd
```

---

- Taking User Input Values and returning the final value
```
def add(num1, num2):  
    result = num1 + num2  
    return result  
  
val_1 = int(input("Enter a number-1: "))  
val_2 = int(input("Enter a number-2: "))  
result = add(val_1, val_2)  
print(f"Result => {result}")

Output Response -
Enter a number-1: 2
Enter a number-2: 3
Result => 5
```

---
---

- Till now, we saw returning single value from the function.
- Is there a possibility that we can return multiple values from the function?
	- Yes, its possible
	- Not with multiple return statement.
	- Instead single return statement with comma separated values
	- Also while receiving we can have multiple result variable where it stores the corresponding values at a particular variable

```
def arithmetic(num1, num2):  
    addition = num1 + num2  
    subtraction = num1 - num2  
    multiplication = num1 * num2  
    return addition, subtraction, multiplication  
  
val_1 = int(input("Enter a number-1: "))  
val_2 = int(input("Enter a number-2: "))  
result1, result2, result3 = arithmetic(val_1, val_2)  
print(f"Addition => {val_1} + {val_2} = {result1}")  
print(f"Subtraction => {val_1} - {val_2} = {result2}")  
print(f"Multiplication => {val_1} * {val_2} = {result3}")

Output Response -
Enter a number-1: 1
Enter a number-2: 2
Addition => 1 + 2 = 3
Subtraction => 1 - 2 = -1
Multiplication => 1 * 2 = 2
```


---
---

- In this section, we saw how to return a function
- If a function doesn't have a return statement, Python internally returns None
	- If we call a function and store it in a variable and look for the output of the value thats stored in that variable and output comes as None, it means the function we have called doesn't return anything

---
---

