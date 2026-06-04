
- In this section, we shall look at if we can pass a function as an argument of another function.
- In Python, we can pass values as arguments as a function and we can pass a function as an argument of another function

```

  
###### REGULAR APPROACH ######
def add_1(number):  
    return number + 1  
  
def square(number):  
    return number * number  
  
num = int(input("Enter a number: "))  
result_1 = add_1(num)  
result_2 = square(result_1)  
print("add function output",result_1)  
print("square function output",result_2)

Output Response -
Enter a number: 3
add function output 4
square function output 16
```

---

```
#### instead of doing the above thing [having 2 different result variables] ####  
# In Python, we can pass a function as argument of another function.  
  
def add1(number):  
    return number + 1  
  
def square(number):  
    return number * number  
  
num = int(input("Enter a number: "))  
result = square(add1(num))  
print("square function output ",result)  
# this approach 1st call the add function and then call the sqaure function

Output Response -
Enter a number: 3
square function output  16
```


---

Not only one function, multiple function can be called as an argument of a function

---
---

