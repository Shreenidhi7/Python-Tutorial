
- This section, we will explore something called regular expression or regex in python.
	- Regex is nothing but a special sequence of characters that defines a pattern for doing complex string matching functionalities.
- Till now what we have seen is 
	- how to create strings
	- manipulate strings
	- calculations/operations on strings
	- check 2 strings are equal with equllity operator
	- find string is present inside another string with membership operator
	- Etc
- String Matching is very common when we deal with programming language and including Python
- We can perform lot of things with strings and using string built in methods
- Sometimes we may need to do some sophisticated pattern matching with strings, in that case we should Regular Expression or RegEx

- In this section, we will learn what is regular expression, how to access the regular expression module in Python [RE module] and how regular expression matching is done in python
- We will look at what are the functionalities or functions available in RE module to do pattern matching against a string.
- We will also learn how to create the complex patterns using the symbols or quantifiers or also known as meta characters.

- Regex could be bit tricky to start with but as we learn about it it would be easy to understand and follow.

```
message = "The current Python version is 3.14"  
  
# Check if "Python", "14" is present in above string  
print("Python" in message)  
print("14" in message)  
print("15" in message)  
  
# Find the index of a character in string  
print(message.find("3.14"))  
print(message.find("Python"))

Output Response -
True
True
False
30
12
```

- In this example, we did a straight forward character by character comparison.
- Sometimes we need to do something extra or more complicated 
	- Rather than searching for a fixed version 3.14, we might need to determine or find whether a string contain any consecutive version of the provided input string.
	- In that case, the straightforward way doesn't work

- message = "The current Python version is 3.14. Other previous versions are 3.13, 3.12, 3.11."
	- In the above string, we just don't want to match 3.14, instead we want 3.13,3.12,3.11 also to be matched
	- In these kind of scenarios, regex will come into picture.

- How to use Regex in python?
	- There is a module called RE module. The Regular Expression functionalies in Python is supported by the RE module in Python
	- The RE module contains many functions that will be useful to do these kind of search oprations.
	- Also it provides a series of meta characters or special symbols and quantifiers to create patterns
		- import re => Way to import RE module
			- There are many functions like search function, match function, match function, find all function, find other functions present in RE
			- The basic function is search function, re.search