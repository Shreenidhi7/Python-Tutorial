
Escape Characters in Python
- Basically these are used when we need to include certain special characters in a string which we cannot otherwise include or it is difficult to include in the string 
- All these escape sequences that we are going to use or see is that they start with the backslash [ \ ]
- We will look at few of the escape sequence that are commonly used in Python
1. \n => Used for New Line/Next Line Character
	1. It moves the cursor to the next line (basically to go to newline)
2. \t => Used for adding a tab. It adds tab b/w characters or words
3.  \\ => Used to insert a backslash [a single backslash]
4.  \' => Used to insert a single quote inside a single-quoted string

Real-Time Examples

1. Backslash n [ \n ]
	1. Print something in a new line
	2. Whenever we want to move some character or a sentence in a new line or anything in a newline inside a string, we can use \n character
	3. Important - It is treated as a single character internally in Python.
```
# 1. \n  
print("Hello Everyone.\nHow are you doing?")

Output Response -
Hello Everyone.
How are you doing?
```

---

2. Backslash t [ \t ]
	1. It inserts a tab between the words or characters where the \t is used.
		1. A bigger space b/w the words/characters
```
# 2. \t  
print("Shree 20")  
print("Shree\t20")

Output Response -
Shree 20
Shree	20
```

---

3. Double Backslash [\\]
	1. Whenever there is a slash [ \ ], python will think that we are writing some kind of escape sequence
	2. In the below example
		1. print("new/old")
			1. There would be a Syntax error - Because python looks for \o in its dictionary as its a escape sequence/character
				1. \o is not a escape character in python - so it throws an error.
				2. To avoid this, we need to use double slash [\\] where the slash is accounted
```
# 3. \\ [Double Slash]  

print("new\old")
Output Response - 
SyntaxWarning: "\o" is an invalid escape sequence. Such sequences will not work in the future. Did you mean "\\o"? A raw string is also an option.
  print("new\old")

---  
print("new\\old")
Output Response - 
new\old

```

One more example - What if i use \n [which represents new line]
```
# 3. \\ [Double Slash]

print("yes\no")
Output Response - 
yes
o

print("yes\\no")
Output Response -
yes\no
```

---

4.  Single Quoted Backslash [ \' ]
	1. Lets say for the below example which is the print statement
		1. In which the statement is written under single quote
			1. print('This is python's lecture')
				1. If we write this in the editor, the editor itself will throw an error.
				2. If we run this code, the execution will throw an syntax error [unterminated string literal]
			2. When we start a single quoted string, python looks for a single quote to finish/terminate/end.
			3. In this example, we have multiple single quotes in the statement, so python doesn't understand where exactly the single quote has ended.
		2. In these situations, we need a Single Quoted Backslash
			1. print('This is Python\'s lecture')
```
#4. \' [Single Quoted Backslash]  
  
print('This is python's lecture')
Output Response -
print('This is python's lecture')
SyntaxError: unterminated string literal (detected at line 23)


print('This is python\'s lecture')
Output Response -
This is python's lecture

```

----

There are few more, for example similar to Single Quoted Backslash, we do have Double Quoted Backslash as well.
This comes into picture when we have a print statement starting with the double quotes.

```
# 5. \" [Double Quoted Backslash]  
  
print("This is python"s lecture")
Output Response -
print("This is python"s lecture")
SyntaxError: unterminated string literal (detected at line 27)


print("This is python\"s lecture")
Output Response -
This is python"s lecture

-----
Example - 2
-----

print("He says, "We are learning python"")
    print("He says, "We are learning python"")
                     ^^^^^^^^^^^^^^^^^^^^^^
SyntaxError: invalid syntax. Is this intended to be part of the string?

print("He says, \"We are leaning python\" ")
Output Response -
He says, "We are leaning python" 

```

---

