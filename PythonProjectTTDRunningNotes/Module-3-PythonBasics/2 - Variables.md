
What are Variables?
1. Variables are "Reserved Memory Locations" that are used to store values.

Why Variables?
1. Example from mathematics 6x + 7y + 2z = 0
	1. In the above expression x, y, z are called variables.
	2. In the above expression 6, 7, 2 are called coefficients
2. These variables x, y, z can have various number of values.

In Python, variables names can have different set of values like Float, Integer or a String.
Also, we can specify as many as variables names we want.
In IDLE, type a = 1 [ =(equals) is called an assignment operator - they are used to assign values ]
```
a = 1
print(a)
1
b = 2
print(b)
2
c = 3
print(c)
3
d = a+b+c
print(d)
6
```

-----

If you don't want a variable, we can even choose to delete them
- syntax = del variable_name
	- del d

```
del d
print(d)
Traceback (most recent call last):
  File "<pyshell#10>", line 1, in <module>
    print(d)
NameError: name 'd' is not defined. Did you mean: 'id'?
```

--------

Now, if we check a,b,c variable still exists after the deletion of variable d.
Yes, it does exist as we have only deleted the variable d.

```
print(a)
1
print(b)
2
print(c)
3
```

---------

**Replacing the same variable with different values**
Initially the variable x is assigned with value 5, later the same variable is replaced with a different value.
x is assigned with value 5 initially, the same x variable is replaced with value 3
At the end, when we print the value for variable x, 3 is printed as the output.

```
x = 5
print(x)
5
x = 3
print(x)
3
```

---

**Multiplication**

```
x = 5
print(x)
5
x = 3
print(x)
3
y = 1
z = x*y
print(z)
3
```

---

**There are some rules & exceptions while creating a variable**
1. The variable name should begin with an alphabet
	1. Example : a = 1
2. The variable name can also begin with underscore and alphabet
	1. Example :  _a = 1
3. The variable name shouldn't be a number
	1. Example : 5 = 1
		1. Syntax Error - Can't assign to literal
4. The variable names are "Case Sensitive"
	1. Example : 
		1. age = 29
		2. print(Age)
			1. name "Age" is not defined
5. The variable name can contain number after the word, but the number at the starting will give us an error
	1. Example:
		1. a1 = 10
		2. print(a1)
			1. 10
6. The variable name can also be a word
	1. Example:
		1. name = "Shree"
		2. print(name)
			1. Shree

---

**Task/Challenge**
I want the word "Hello World" to be printed.

Solution - 
```
Type - 1 
print("Hello World")
Hello World

Type - 2
word = "Hello World"
print(word)
Hello World

Type - 3
a1 = "Hello"
a2 = "World"
a3 = a1 + a2
print(a3)
HelloWorld
```


------

