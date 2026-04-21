
**Type Conversion/Type Casting in Python**
1. As the name suggests, converting data type from one to another.
	1. If the data is in one data type, we can convert it into another data type

```
# Converting Interger into Float
num1 = 100
num1
100
type(num1)
<class 'int'>

num2 = float(num1)
num2
100.0
type(num2)
<class 'float'>
```

```
# Converting Float into Integer
num3 = 56.75
num3
56.75
type(num3)
<class 'float'>

num4 = int(num3)
num4
56
type(num4)
<class 'int'>
```

* Question 
	* We have a float value 77.85.
	* When we convert it to Int, will the value be 77 or 78?
* Answer
	* The value would be 77 after converting the float value (77.85) yo int.
	* We are just converting the float value to int value, we are not rounding off the value.
	* So the converted value will be 77

```
# Converting Integer into String
num5
1000
type(num5)
<class 'int'>

x = str(num5)
x
'1000'
type(x)
<class 'str'>
```

Important Note - Type Casting will not change the existing variable value.

```
# Converting Float into String
num6 = 12345.67890
num6
12345.6789
type(num6)
<class 'float'>

y = str(num6)
y
'12345.6789'
type(y)
<class 'str'>
```

Can String be converted into Int & Float?
* Character is the String ["Hello"]
	* Try to convert the value which is inside the quote "Hello" to an integer, but the conversion cannot happen with "Hello" characters
		* Characters inside the string -> convert it into an integer -> it won't work
	* Similarly, if we try to convert the same string into a float - it won't work either.
```
# Conversion of Characters in a String to Int & Float
s1 = "Hello"
s1
'Hello'
type(s1)
<class 'str'>

a = int(s1)
Traceback (most recent call last):
  File "<pyshell#43>", line 1, in <module>
    a = int(s1)
ValueError: invalid literal for int() with base 10: 'Hello'

b = float(s1)
Traceback (most recent call last):
  File "<pyshell#45>", line 1, in <module>
    b = float(s1)
ValueError: could not convert string to float: 'Hello'
```

* Digits in the String ["12345"]
	* ["12345"] is a string, but all the characters are Digits.
		* The conversion from String to Integer works without any errors
	* If a string contains properly digits inside it, we can convert that value into a string.

```
# Conversion of Digits in a String to Int & Float
s2 = "12345"
s2
'12345'
type(s2)
<class 'str'>

x = int(s2)
x
12345
type(x)
<class 'int'>

y = float(s2)
y
12345.0
type(y)
<class 'float'>

```

Cases where the conversion from String to Int/Float is not possible

```
int("Python3.14.3")
Traceback (most recent call last):
  File "<pyshell#61>", line 1, in <module>
    int("Python3.14.3")
ValueError: invalid literal for int() with base 10: 'Python3.14.3'
float("Python3.14.3")
Traceback (most recent call last):
  File "<pyshell#62>", line 1, in <module>
    float("Python3.14.3")
ValueError: could not convert string to float: 'Python3.14.3'

int('python3')
Traceback (most recent call last):
  File "<pyshell#64>", line 1, in <module>
    int('python3')
ValueError: invalid literal for int() with base 10: 'python3'
float('python3')
Traceback (most recent call last):
  File "<pyshell#65>", line 1, in <module>
    float('python3')
ValueError: could not convert string to float: 'python3'

int('123a')
Traceback (most recent call last):
  File "<pyshell#67>", line 1, in <module>
    int('123a')
ValueError: invalid literal for int() with base 10: '123a'
float('123a')
Traceback (most recent call last):
  File "<pyshell#68>", line 1, in <module>
    float('123a')
ValueError: could not convert string to float: '123a'

int('123-')
Traceback (most recent call last):
  File "<pyshell#70>", line 1, in <module>
    int('123-')
ValueError: invalid literal for int() with base 10: '123-'
float('123-')
Traceback (most recent call last):
  File "<pyshell#71>", line 1, in <module>
    float('123-')
ValueError: could not convert string to float: '123-'

```

---

We have a variable called language = "Python" and version = 3.14
Lets consider a scenario where we want to combine both this together. The output we want is Python3.14

String Concatenation is something that could be performed.

Can we do : language + version ?
* No we cannot do it because the system throws a "Type Error" [Can Only Concatenate str (not "float") to str]
	* Means we can only concatenate string and string types
	* We wont be able to concatenate string and float
* string + float :: Addition operator (+) (Plus Operator) works as mathematical addition
* But with string - Addition operation works as a concatenation or joining operation/join operation
	* So with String & Float - there is a mismatch - Python gets confused -> In this state, Python gives an error called "Type Error"

```
language = "Python"
version = 3.14
Required Output - Python3.14
language+version
Traceback (most recent call last):
  File "<pyshell#76>", line 1, in <module>
    language+version
TypeError: can only concatenate str (not "float") to str
```

* Question
	* What can we actually do in order to get the output Python3.14?
* Answer
	* This can be possible by using "Type Casting/Type Conversion" method.
* How?
	* If we see **Python** is a string and i want to join **3.14** to Python.
		* Then i want the value 3.14 to be a string as well.
	* So Can we convert **3.14** into a String?
		* Yes, we can do that by converting 3.14 into string.
		* In that case both "Python" & "3.14" would be of type string
			* So both variables can be concatenated.

```
language = "Python"
version = 3.14
Required Output - Python3.14
language + str(version)
'Python3.14'
```

---

* What do we get if we perform "100" + "100"? Will we get 200?
	* No, the output would be 100100
		* Because both of these are strings.
* What if i want to add both of them "100" + "100", to get 200 as output?
	* I need to convert both of them to int first and then add them
		* Output would be 200

```
'100' + '100'
'100100'
int('100') + int('100')
200
```

---
