
Strings are group of characters enclosed within quotations
Until now, we have seen
- how to create stings
- how to find out the length of the string by using the len function
- how to do indexing on strings
- how to perform slicing on strings

Now, we will look at other operations on strings.
Lets take an example where we create a string called "Python is Fun"

We shall simply revise before checking other operations on strings
```
s1 = "Python is fun"  
  
# First character of the string  
print(s1[0])  
  
# Last character of the string  
print(s1[-1])  
  
# Length of the string  
print(len(s1))  
  
# String Concatenation [Plus operator acts as a concatenation operator]  
language = "Python"  
version = "3.13.3"  
print(language+version)

Output Response - 
P
n
13
Python3.13.3
```

---
We know that, if we perform the addition/concatenation [ + ] operation on 2 strings, the 2 string gets attached together to form one compound string.
But, what happens if we perform the subtraction [ - ] operation for the 2 strings?
- print("Python" - "p")
- It gives an error saying "Unsupported operand type(s) for - : 'str' and 'str' "
- The minus [ - ] operator is not supported in python with strings

----
What about the "Multiplication" operator?
- Lets say we have a variable declared with string value
	- [s1 = "Python"]
	- print(s1 * 3)
- What should happen with the multiplication perform along with string value?
- Output -> PythonPythonPython
- Because multiplication [star **] operator is the repetition of strings
- In Strings,  '*' is repetition operator
- So Python is repeated 3 times, without any space in between
```
# String Repetition [Multiplication]  
print(language*3)
Output Response -
PythonPythonPython
```

----

**Checking of membership/ Membership operation in Strings**
- There is an operator called [ in ] in python which checks if a string or a character is part of another string or not.
- Example -
	- s1 = "Python is fun"
	- print("Python" in s1)
- We are checking that - Is the string "Python" present in s1
- If Python is present in the string s1 - we get the output as True
- If Python is not present in the string s1 - we get the output as False
```
# Membership operation  
# in  

s1 = "Python is fun"  
print("Python" in s1)

Output Response - 
True
```

- We can check for string or even the character as well
```
# Membership operation  
# in  

s1 = "Python is fun"  
print("i" in s1)

Output Response - 
True
```

- What happens if we check the character which is not present in the variable?
	- We get the output as False
```
# Membership operation  
# in  

s1 = "Python is fun"  
print("z" in s1)
print("Java" in s1)

Output Response - 
False
False
```

The [in] operator is called a membership operator which checks the membership of any string or a character inside another string.

There is another membership operator [not in] - its just opposite of [in] operator.
```
s1 = "Python is fun"  

# Expect False  
print("Python" not in s1)  
print("i" not in s1)  

# Expect True  
print("z" not in s1)  
print("Java" not in s1)

Output Response - 
False
False
True
True
```

Another thing to note here is [ in ] and [ not in ] are case sensitive operators
It should be written in small case.

----
---

Comparison of Strings
- Equality Operator [ == ]
- Examples -
	- print("Python" == "Python")
		- True
	- print("Python " == "Python")
		- False [Because there is a space after Python in the first comparison operand]
			- Since spaces are also considered as characters in string, we cannot ignore them.
			- But because of some reason there are unnecessary spaces present in the string which may lead to some wrong results
```
# Comparison operator  
print("Comparison Operators - Equality")  
print("Python" == "Python")  
print("Python " == "Python")

Output Response -
True
False
```

In order to take care of the tailing or leading spaces around the string, there is a function called "strip"
Removing spaces from a string - strip()
- Strip will remove any initial spaces and any trailing spaces from any string
Example - 
- s1 = "Python"
- s2 = s1.strip()
	- We are using a function called strip() on s1 and we are storing the result in s2
- print(s2)
```
# Removing spaces form a string - strip()  
s1 = "Python "  
s2 = s1.strip()  
print(s1)  
print(s2)

Output Response - 
Python 
Python
```

Now, if we compare the below
- s1 = "Python "
- print(s1.strip() == "Python")
- Output - True
	- s1.strip() has removed the trailing spaces and then compares with "Python", hence the output is True
	- It also removes all the trailing and leading spaces
		- s1 = "                   Python           "
		- print(s1.strip())
			- Output -> Python

---
---

Replace Function [replace()]
- Replace function is used to replace a part of a string or a character from a string.
- Example - 
	- s1 = "We are learning Python"
- Now, we want to change Python to Java
- Replace function replaces the Python from the string s1 and changes it to Java
```
# Replace a String or a part of the String [replace()]  
print("Replace String")  

s1 = "We are learning Python"  
print(s1)  
print(s1.replace("Python","Java"))
print(s1)

Output Response - 
We are learning Python
We are learning Java
We are learning Python
```

---
**Important Note**
One thing to note here is , if we use any function such as replace with string, the existing string doesn't change.
Replace will just replace and give a new output
It doesn't re-assign/changing the existing string, we are getting a new string

---
One more example

```
s1 = "We are learning Python"  
print(s1)  
print(s1.replace("e","E"))  
print(s1)

Output Response - 
We are learning Java
**WE arE lEarning Python**
We are learning Python
```

If we observe carefully, all small "e" are replaced with capital "E"
By default, if we use a replace function with a string, wherever it finds the argument, everywhere the value will be replace with new value

----

Is there a way we can replace only one occurrence?
- Yes with the parameter available in the replace function - count
- If we provide the count as 1 - then only the 1st occurrence will be replaced with new value, rest all occurrence remains as it is.
```
s1 = "We are learning Python"  
print(s1)  
print(s1.replace("e","E",count=1))  
print(s1)

Output Response - 
We are learning Python
**WE are learning Python**
We are learning Python
```

----

