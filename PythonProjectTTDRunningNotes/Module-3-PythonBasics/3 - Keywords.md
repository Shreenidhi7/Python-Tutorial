
In any language, for example English,  if we are trying to frame a sentence or talk to someone, we need some words.
Any word that is defined in any language for that matter has a meaning to it.
It has certain understanding in that language.

Similarly in Python, the keywords are "**Special Reserved Words**".

Like in English, we have a dictionary.
In dictionary we have a English word and a meaning to them.

Similarly in Python or any other programming language have a word which has a special meaning to it and they are reserved.
Also it has some purpose that it performs in the language.
And it cannot be used for any other purpose in the language.

Example - We saw when we are looking at variables that variable we define during which we cannot use keywords as variables
When we used a keyword as a variable name - it fails and gives an error.

What are the keywords in Python?
1. for, while-> used to write loops in python
2. break -> 
3. continue ->
4. def and lambda -> used to create functions in python.
5. and, or, not -> logical operators in python
6. True, False, None -> literal keywords in python

These keywords are called the vocabulary of the programming language.
The keyword should be used for that particular purpose only for which it is reserved
It should not be used for any other purpose

Example - 
* What happens if we use these keywords are variable name?
	* The complier throws an error.

```
break = 5
SyntaxError: invalid syntax
True = Yes
SyntaxError: cannot assign to True
continue = 10
SyntaxError: invalid syntax
False = No
SyntaxError: cannot assign to False
```

---

Question
* Where do these "keywords" come from?
Answer
* When we install Python, these keywords come with the installation.
* We don't have to do anything extra to use these keywords in our program.

---

Question
* What is that we need to do if we want to know all the available keywords that is present in the current version that is installed?
Answer
* We cannot directly look at all the keywords available.
* If needed, we can look at the documentation of python
* But if we want to see the keywords available in the current version, we can actually use a program/command to list the keywords available

1. import keyword 
	1. We are importing the module in python called keyword
	2. This keyword module has the information of the keywords that is there in python in current version.
2. keyword.kwlist
	1. Using the "keyword" module, there is a variable called kwlist which basically stores all the names of the keyword that is present in the current version of python.
	2. Once pressed enter, we will see the list of keywords available in the current version of python [3.14.3]

```
import keyword
keyword.kwlist
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```


----

**Summary - Keywords are nothing but a pre-defined words used in any programming language.**

---
