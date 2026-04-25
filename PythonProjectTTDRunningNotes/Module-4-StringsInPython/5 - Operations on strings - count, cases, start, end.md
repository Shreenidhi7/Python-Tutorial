
In the previous section, we discussed about certain operations in strings
- How to repeat string
- How we can replace certain characters or substring from a string
- How to check the membership of the string

In this section, we shall continue looking at the operations on strings.
Functions like
- Count function
- How to find something is at the start/end of the string
- How to convert a string into cases/changing cases of strings
	- Uppercase
	- Lowercase

---
---

**Counting Substring from a String**
- In order to count the substring from a string, we have a count function.
- Its basically used to count the number of occurrences of a string or a substring or a character inside a main string or a substring.
- Function - count()
- Syntax - string.count(substring)
	- How many times the substring is present in the string, the count function will count that.
- Example -
	- s1 = "We are learning Python. Python is fun."
	- s2 = "Python"
	- If we want to check, how many times the substring "Python" is present in the string s1.
	- print(s1.count(s2))
		- 2 [Because Python is present 2 times in the string s1 ]
```
s1 = "We are learning Python. Python is fun"  
s2 = "Python"  
print(s1.count(s2))
print(f"Occurrences of {s2} is {s1.count(s2)}")

Output Response - 
2
Occurrences of Python is 2
```

Instead of checking a substring, we can check with the characters as well
```
s1 = "We are learning Python. Python is fun"  
s3 = "e"  
print(s1.count(s3))  
print(f"Occurrences of {s3} is {s1.count(s3)}")

Output Response - 
3
Occurrences of e is 3
```

Now, we have "learning" in s1, but if we have count the occurrence for "learn". Will it count?
- Yes it will count.
	- Remember, it will not count words, it counts any character combination is the same sequence

```
s1 = "We are learning Python. Python is fun"  
s4 = "learn"  
print(s1.count(s1))  
print(f"Occurrences of {s4} is {s1.count(s4)}")

Output Response - 
1
Occurrences of learn is 1
```

Even the empty - spaces could also be counted.
```
s1 = "We are learning Python. Python is fun"  
s5 = " "  
  
print(s1.count(s5))  
print(f"Occurrences of empty-spaces is {s1.count(s5)}")

Output Response -
6
Occurrences of spaces is 6

```

Summary -  Count function counts how many times a particular character or a substring is present in another string.

---
---

**Cases of Strings in Python** [Changing case of a string]
- There are multiple functions such as "Upper"/"Lower"/"Title"/"Capitalize"
	- upper()
	- lower()
	- title()
	- capitalize()

Uppercase Conversion
- s1 = "Python"
- print(s1.upper())
- Output - PYTHON
	- Python is a mix of upper and lower case [1st character is in uppercase, rest all in lowercase]
	- If we perform s1.upper() -> all the characters will be converted to uppercase
```
a1 = "Python"  
print(a1.upper())
Output Response - 
PYTHON
```

What happen if we have characters like 3.14 with the string, can we convert digits into uppercase?
- No we cannot, we don't have uppercases or lowercases in numbers or digits.
What happens if we have the digits in a string and try to uppercase it? Will it throw an error?
- No, it doesn't give an error.
The non-alphabetical character when tried to upper/lower case remains the same, only the alphabetic characters gets converted to upper/lower case

---
Lowercase Conversion
- Lowercase converts the entire string into lower case.
- In the string "Python3.14", only P is capital and rest of the characters are small letter, so everything will be converted into small/lower case.
```
a1 = "Python3.14"  
print(a1.lower())

Output Response - 
python3.14
```

---
Upper and Lower Case Conversion

```
a2 = "We are learning Python. Python is fun"  
print(a2.upper())  
print(a2.lower())

Output Response - 
WE ARE LEARNING PYTHON. PYTHON IS FUN
we are learning python. python is fun
```

----

**Title Conversion**
- All the first characters of the words will be converted into upper case
- Example - 
	- a2 = "We are learning Python"
	- print(a2.title())
		- We Are Learning Python
```
a3 = "We are learning Python again and again"  
print(a3.title())

Output Response - 
We Are Learning Python Again And Again
```

---

**Capitalize**
- Capitalize only keeps the first letter of the entire string as capital letter and all other characters become lower case.
	- If any character in-between is capital, it will convert that to lower case as well.
	- It shall keep only the 1st character of the entire string as capital and everything else as small letters
- There is a minor difference b/w title() and capitalize()

Title() -> It will make all the first letter of the words as capital.
Capitalize() -> It will make only the first character of the entire string as capital.

```
a4 = "We are learning Python again and again. Python is REALLY FUN!!"  
print(a4.capitalize())

Output Response -
We are learning python again and again. python is really fun!!
```

----
---

**Starts/Ends with** [Starting and Ending of a String]

1. Startswith()
	1. This function will check if a string is starting with another substring or not.
	2. Syntax => string.startswith(substring)
	3. If the condition matches, it returns True, else it returns False
	4. Its case sensitive as well. It looks for the exact match\
```
b1 = "We are learning Python"  
print(b1.startswith("We are"))  
print(b1.startswith("we"))

Output Response - 
True
False
```


2. Endswith()
	1. Similar to startswith()
	2. It will check if a particular string ends with a substring or not
	3. Syntax => string.endswith(substring)
	4. If the condition matches, it returns True, else it returns False
	5. Its case sensitive as well. It looks for the exact match
```
b1 = "We are learning Python"
print(b1.endswith("Python"))  
print(b1.endswith("n"))  
print(b1.endswith("Pytho"))

Output Response - 
True
True
False
```

----
---
