
In any programming language, we need to understand the basic building blocks of that programming language.
These building blocks are called components of programming language.
The 1st component that we will look at in this section are "Literals"

Literals is defined as a value or data that are used while we write any program.
Ex: When we write a program -> the program can consist of a number of data.
1. Name
2. Age
3. Phone Number
4. Address
All these are nothing but certain data. So the "Data" that is involved in our program is called "Literal"
* Name = Shree
* Age = 29
* Phone Number = 9876543210
* Shree is student and he studies 5 subjects.
All these information are nothing but "Data"

-----

Lets open the Python's IDLE and understand the "Literals"
	- Search for IDLE in window's search bar [IDLE appears only if the python is installed in the system]

Before we start, lets configure out IDLE
1. Open IDLE
2. Go to "Options" -> "Configure IDLE"
3. Increase the Font Size for Better Visibility [Increase it to 16]

Now, when certain data is required for example Shree is a data, Age is a data.
So we can classify data in different types
Example:
1. Numbers/Numeric Data [Could be Whole Numbers/Fraction Numbers]
	1. Whole Numbers
	2. Fractional Numbers
2. String Data
3. Boolean Data
4. None Data

So, in IDLE if we write 1000 and press enter, then the IDLE return 1000
If the IDLE doesn't give any error, then it means it has worked properly
- 1000 is a numeric value - Its called a "Numeric Literal"
	- The Specific Name of this is "Integers"

What are Integers?
- Integers are nothing but Whole Numbers
	- What are Whole Numbers?
		- Non-Fractional numbers are called as Whole Numbers
- So 1000 is a Numeric Literal specifically an "Integer"
- Integers can be positive numbers/negative numbers or zero(0)
- When we write -500 in IDLE, it returns the same value -500

The Second Type of Numerical Literal is "FLOAT"
What is a FLOAT?
* Float is defined as the numbers which are fractional or have decimal points.
* Example - 
	* pi value - 22/7 - 3.14 is a float
	* Marks Percentage - 98.3  - Its a float value
* Python supports "Negative numbers with decimal points" aswell
	* Example - 
		* Temperature : -5.32 degree Celsius

Question
1. What is 10.0. How is it classified?
	1. Answer -  Its is classified into "Float" and not into an "Integer"
		1. Because we have a "Decimal Point"
		2. Any number, even if the value after decimal point is zero(0) [10.00]
			1. It is considered as Floating point value

Real Life Examples of Integers and Floating Point Values
1. Integers
	1. Integer Literals can be used to store some kind of a phone number [9876543210]
	2. Person's Full Age [29]

2. Floating Point Literal
	1. Float Literals can be used to store some person's marks/percentage [98.5]

These two [Integers[Whole Numbers] / Float Literal[Fractional Numbers]] are the Numerical Literals

---------

**String Literals**

1. String Literals are used for basically storing some kind of names, messages, paragraph, sentences etc...
2. String Literals - They are nothing but a sequence of a group of characters
	1. Example:
		1. Hello
			1. If we type **Hello** directly in the IDLE, it will throw an error
				1. Python says **Hello** is not defined.
3. One Important thing about "String Literals" is that they should be enclosed with "Quotes"/"Quotations"
	1. It could be Single Quote (' ') / Double Quote (" ") / Tripe Quote (''' ''') (""" """)
		1. Example -
			1. Single Quote - 'Hello'
			2. Double Quote - "Hello"
			3. Tripe Quote - '''Hello''' or """"Hello"""
	2. These are 4 ways we can create "String Literals" - Only the quotations differ
4. There is a catch here
	1. What happens if i start with single quote and end with double quote - 'Hello"
		1. There would be a syntax error - unterminated string literal
5. A "String Literal" can be a sentence as well
	1. Example - "Hello Everyone, i am learning Python."

Question?
	1. Why/When do we need Triple Quotes?  [ Tripe Quote - '''Hello''' or """"Hello""" ] Where could we use it?
			1. Answer - If we want to create multi-line strings, then single quote and double quote won't work
				1. To write multi-line string values, we either have to use "Single Quoted Triple Quote" [''' haha '''] or "Double Quoted Triple Quote" [""" hehe """]
				2. Response from IDLE -
```
""" Hello,
How are you?
Lets learn python """
' Hello,\nHow are you?\nLets learn python '
```

Now, one thing we can observe here form the output
1. We wont see the output in different lines, rather we see it in a single line
	1. Wherever there is "next line" used, something like [slash n (\n)] is used.
	2. This [slash n (\n)] is a special character in Python which is used to represent the "New Line" or the "Next Line"
		1. This is also called as a "Escape Sequence" or the "New Line Character"
		2. Both [slash n (\n)] together are called "New Line" or "Next Line" character

---

**Boolean Literals**

1. Boolean Literals have only 2 values in them
	1. True
	2. False
2. As the name suggests, Boolean literals are used to represent the cases where the user have to check certain conditions
	1. T & F are in capitals [ Case Sensitive ]
		1. In IDLE, if we write True with capital T -> it works well
		2. In IDLE, if we write False with small f -> it will throw an error [ as true/false cannot be identified/recognized by Python]


---

**Special Literal [None]**

1. None is said to be a special literal which is used to represent "No Value" or an "Empty Value" or an "Null Value" - Its means its not value
2. There are situations wherein you do not know what the value is
	1. You don't know whether its a Number,  Name, Age - In these cases we use "None"
3. None also represented as N capital - None [ Case Sensitive ]
4. When you type None in IDLE, you wont get any response in return because represents nothing.

-------
