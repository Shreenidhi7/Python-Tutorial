
This section is the continuation of the previous section where the Type Conversion/ Type Casting was discussed on int,float,str.
Basically we converted few of the integers into strings, float into strings
- If its a valid digits as characters in a string, we can convert into an integer.
	- Example - int('10123')
		- Output - 10123
- If its a valid float value inside the string, then it also can be converted into a float.
	- Example - float('78.45')
		- Output - 78.45

In this section we shall what shall happen 
1. if we typecast something to Boolean?
	1. Int, Float, String, None
2. If we typecast Boolean to a different data type?

```
# Conversion of Bool to String
val1 = True
val1
True
type(val1)
<class 'bool'>

str(val1)
'True'

# Conversion of String to Bool
bool("Python")
True

# Conversion of Int to Bool
bool(100)
True

# Converison of Float to Bool
bool(1.5)
True
```

---

Question
- Is that whatever value we try to convert to Bool, will provide the bool value as True?
Answer
- Not everything, below is an example where the converted bool value is False
- bool(0) [Int]
	- False
		- Reason - False is the value which is used to represent which doesn't exist
- bool(0.0) [False]
	- False

Tricky Question
- What happens when you try a negative int value to convert to Boolean?
	- Will it be True or False?
Answer
* The answer is True, False is only when the value is 0
	* bool (-100)
		* True

```
bool(0)
False

bool(0.0)
False

bool(120)
True

bool(-120)
True

bool(-10.5)
True

bool(0.5)
True
#since 0.5 is some quantity, the bool value returned is True
```

**Both positive and negative integers and positive and negative floats will give you True value when you convert it into a Boolean data type**

**Only 0 & 0.0 in terms of numbers will give you a False, Apart from this for other values it will be True**

---

Question
* What about the Strings when converted to Boolean?
Answer
* When we convert the string "Python" to boolean, it gives True
	* bool("Python")
		* True
* With the single character "a" when converted to boolean,  will also return True.
	* bool("A")
		* True
* Even an space when converted to boolean, will return True [ Because space is a valid character ] 
	* bool(" ")
		* True
* Any valid string character when converted to Boolean, will return True
	* Hyphen, Percentage, Underscore - All these are valid characters including Space.

```
bool("Python")
True

bool("A")
True

bool(" ")
True
```


Question
* Does it mean that there is no string that will give us FALSE when we convert to Boolean?
Answer
* No, there is something - Its called EMPTY STRING
	* Nothing inside the quotes are referred as Empty String
		* Just a pair of single/double/triple quotes or double triple quote [Nothing in middle of the quotes]
			* Example - '',"","""""",
		* If we create a string with quotes and don't write any character{not even space} - Its called an empty string.
	* When we convert EMPTY STRING to Boolean, then we get FALSE.

```
bool('')
False

bool("")
False

bool("""""")
False
```

---

We observed that 0[Integer], 0.0[Float], ''[Empty String] - If we try to convert these 3 to boolean, we get FALSE

Any other value apart from this, we will get a True
* Be it Negative Numbers, Positive Numbers, Both Float & Integer, Any Character, Any Sentence, Any Word, Even Spaces and Special Characters 
	* If we try to convert them to Boolean or typecase them to Boolean - We get a TRUE

---

Question
* We are left with one more value - Its None
* What about None?
* Will we get a TRUE/FALSE when converted to Boolean?

Answer
* None is a value,but None is used to represent NO VALUE/EMPTY VALUE
* So when None converted to Boolean, it should be FALSE
	* Example - bool(None)
		* False

```
bool(None)
False
```

---

So, in summary,  0[Integer], 0.0[Float], ''[Empty String], None - If we try to convert these 4 to Boolean, we get FALSE

---

**Boolean to Integer**

* Convert Boolean True to Integer Value
	* When we convert any integer to a boolean
		* int(True)
			* 1
		* int(False)
			* 0


```
int(True)
1

int(False)
0
```

---

**Boolean to Float**

* Convert Boolean True to Float Value
	* When we convert any float to a boolean
		* float(True)
			* 1.0
		* float(False)
			* 0.0
```
float(True)
1.0

float(False)
0.0
```

---

**Boolean to String**

```
str(True)
'True'

str(False)
'False'

str(None)
'None'

```

----
