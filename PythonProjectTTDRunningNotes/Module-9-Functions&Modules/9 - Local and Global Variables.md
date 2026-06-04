
- This section, we shall look at the scope of variables in Python.
- Local Variable
	- We can access this variable only inside a function and cannot access this variable outside the function
- Global Variable
	- We can access this variable outside as well inside the function

GLOBAL and LOCAL 
```
n = 1   # GLOBAL VARIABLE  
  
def fn():  
    n = 5    # LOCAL VARIABLE  
    print("in",n)  
fn()  
  
print("out",n)

Output Response -
in 5
out 1
```

GLOBAL
```
n = 1   # GLOBAL VARIABLE  
  
def fn():  
    print("in",n)  
fn()  
  
print("out",n)

Output Response -
in 1
out 1
```

---

Important
- If we want to change the GLOBAL variable from the function, then there is a keyword in python called "global"
	- We can use this keyword to assign the local variable value to the global variable.

----

```
print("GLOBAL AND LOCAL VARIABLES")  
n = 1   # GLOBAL VARIABLE  
  
def fn():  
    n = 5    # LOCAL VARIABLE  
    print("in",n)  
fn()  
  
print("out",n)  
  
print()  
###########  
print("GLOBAL VARIABLE")  
n = 1   # GLOBAL VARIABLE  
  
def fn():  
    print("in",n)  
fn()  
  
print("out",n)  
  
  
############  
print()  
"""  
Important  
- If we want to change the GLOBAL variable from the function, then there is a keyword in python called "global"  
    - We can use this keyword to assign the local variable value to the global variable."""  
print("ASSIGN LOCAL VARIABLE TO GLOBAL VARIABLE")  
n = 1   # GLOBAL VARIABLE  
  
def fn():  
    global n  
    n = 5    # LOCAL VARIABLE  
    print("in",n)  
fn()  
  
print("out",n)

Output Reference -
GLOBAL AND LOCAL VARIABLES
in 5
out 1

GLOBAL VARIABLE
in 1
out 1

ASSIGN LOCAL VARIABLE TO GLOBAL VARIABLE
in 5
out 5
```

---

Important -
- The most preference is given to the LOCAL variable