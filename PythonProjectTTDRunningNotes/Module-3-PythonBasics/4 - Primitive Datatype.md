
What are Data Types?
* As the name suggest, types of data that are being used inside our program for manipulation and storing purpose
* As we know, when we write a program, we need to store a lot of data in form of someone's Age, Name,  Numbers, Messages so on and so forth.
* So Python classifies these data into certain types.
* We shall look on the Primitive or the Fundamental datatypes

Primitive Datatypes
1. Integers
2. Floats
3. Strings
4. Boolean
5. None

----

**Integers**
- Integers are the whole numbers
- Example -
	- age = 25
		- 25 is the whole number which gets stored in the variable called age
- Question
	- When we wrote this code - assigning integer value (25) to a variable (age). Did we anywhere mentioned that it is a Integer data. Why is that?
- Answer
	- We didn't. Its because Python doesn't require us to write what kind of data it is, whether it is an Integer or Float or String.
	- Python by virtue - By the type of the data itself, it understands during execution what kind of data/ what type of data is provided.
	- The "Type" is checked during the execution of the program.
- Python understands internally that what kind of data it is, but if we want to check what kind of data it is, we can check that too.
- Python provides a function called "type" which can be used to check the data type of the particular variable
	- type(age)
	- <class 'int'>
		- int is a representation of integers in python.

```
# Integers
age = 25
age
25

type(age)
<class 'int'>
```


---

**Floats**
1. Floats are nothing but the decimal point values or fractional values

```
# Floats
percentage = 98.3
percentage
98.3

type(percentage)
<class 'float'>
```


We can even perform multiple mathematical operations with integers and float or between integers and float.
Example -
```
# Addition b/w 2 integers values
10 + 10
20
# Addition b/w 2 floating point values
2.5 + 3.5
6.0
# Addition b/w integer value and float
4 + 3.5
7.5
```

```
a = 10
b = 2.2
c = a + b
print(c)
12.2
type(c)
<class 'float'>
```


---

**String**
1. Strings are group of characters enclosed within quotations.
2. Type -> str is the representation of Strings in Python

```
name = "Shree"
name
'Shree'

type(name)
<class 'str'>

full_name = "Sandal Wood"
full_name
'Sandal Wood'

type(full_name)
<class 'str'>
```


---

**Boolean**
1. As we have understood in Literals, Boolean have 2 values
	1. True & False
	2. True represents a positive scenario, wherein the answer is kind of "Yes" or Positive Answers
	3. False represents a negative scenario, where the answer is "No" or Negative Answers
	4. T an F should be capital.
	5. bool is the representation of Boolean data type

```
val1 = True
val1
True
type(val1)
<class 'bool'>

val2 = False
val2
False
type(val2)
<class 'bool'>
```


---

**Special Data Type [None]**
1. None data type is the data type which stores the value which is not known/empty/has no value/null value
2. NoneType is the representation of None data type

```
val3 = None
val3
type(val3)
<class 'NoneType'>
```


----
