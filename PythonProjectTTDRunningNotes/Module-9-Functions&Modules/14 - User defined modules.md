
- In last lecture, we looked at modules in python and few examples of built-in modules in python.
	- How to import and different ways of importing modules and giving alias to our modules while import.
- This lecture, we will look at creating Python modules
	- To create a python module, we create a file in .py extension and we write our program in that.


---

1. Module -> ArithmeticModule.py
```
"""  
A simple arithmetic module => arithmetic.py  
"""  
  
def add(x, y):  
    return x + y  
  
def square_root(number):  
    return number ** 0.5
```


---

2. User Defined Module Call -> UserDefinedModules.py
```
# importing all the available functions from arithmetic module  
import ArithmeticModule  
  
# Using Add function from Arithmetic Module  
a = 100  
b = 20  
addition_result = ArithmeticModule.add(a, b)  
print(f"Addition of {a} and {b} is {addition_result}")  
  
# Using SquareRoot function from Arithmetic Module  
square_root_result = ArithmeticModule.square_root(a)  
print(f"Square root of {a} is {square_root_result}")  
square_root_result = ArithmeticModule.square_root(b)  
print(f"Square root of {b} is {square_root_result}")

Output Response -
Addition of 100 and 20 is 120
Square root of 100 is 10.0
Square root of 20 is 4.47213595499958
```


---
---

- importing all the available functions from arithmetic module  
	- import ArithmeticModule  
  
- importing specific functions from the arithmetic module  
	- from ArithmeticModule import add  
	- from ArithmeticModule import square_root  


---
---

```
# # importing specific functions from the arithmetic module  
from ArithmeticModule import add  
from ArithmeticModule import square_root  
  
# Using Add Function  
a = 100  
b = 20  
add_result = add(a, b)  
print(f"Addition of {a} and {b} is {add_result}")  
  
# Using SquareRoot function  
squrt_result = square_root(a)  
print(f"Square root of {a} is {squrt_result}")  
sqrt_result = square_root(b)  
print(f"Square root of {b} is {sqrt_result}")

Output Response -
Addition of 100 and 20 is 120
Square root of 100 is 10.0
Square root of 20 is 4.47213595499958
```

---
---
