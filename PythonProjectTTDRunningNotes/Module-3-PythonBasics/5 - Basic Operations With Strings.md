
In this section, we shall look in a bit of details about Strings.
1. How to find the length of the String?
2. What is Indexing?
3. How to join/combine String together?

In IDLE, lets look at the examples

**Different ways to create a String**

```
s1 = "Hello World"
s1
'Hello World'
type(s1)
<class 'str'>

s2 = 'We are learning Python'
s2
'We are learning Python'
type(s2)
<class 'str'>

s3 = """Hello Everyone,
We are looking at Strings
Bye"""
s3
'Hello Everyone,\nWe are looking at Strings\nBye'
type(s3)
<class 'str'>
```

---

**Length of the String**

1. Length of the String means that how many characters are there in the string
	1. Example : s4 = "Python"
		1. How many characters are there in a word/string "Python"
			1. The answer is 6
		2. There is function in Python called "Length" - represented as "len"
		3. In python if we have to use any function, then we have to use a pair of brackets and inside a pair of brackets, we have to use the argument for which we want to find the length of. In our case its s4
			1. Example: len(s4)
				1. Output - 6

```
s4 = "Python"
len(s4)
6

s1 = "Hello World"
len(s1)
11
# - It 11, beacuse there is a space b/w Hello & World - Space is a valid character in Python. Space should be counted as one character

s2 = 'We are learning Python'
len(s2)
22

s3 = """Hello Everyone,
We are looking at Strings
Bye"""
s3
'Hello Everyone,\nWe are looking at Strings\nBye'
len(s3)
45
# Here \n (Escape Character/New Line Character/Next Line Character) is considerd as one character [\n is counted as one character]

```


---

**Indexing**

1. Indexing means positioning.
	1. To understand Indexing, we have to understand one thing in Python.
		1. Every String that we create - exampe s4 = "Python" - It has a internal position assigned to every character of that string.
			1. Example: "Python"
				1. Each character will have its own numbers starting from 0(Zero)
					1. P - 0 [Index of 0]
					2. Y - 1 [Index of 1]
					3. T - 2 [Index of 2]
					4. H - 3 [Index of 3]
					5. O - 4 [Index of 4]
					6. N - 5 [Index of 5]
				2. Every character will have its own position - That's called Index
	2. Indexing means the process of fetching a particular character using its index/position.
	3. How to do Indexing?
		1. Indexing is done using "square brackets"
			1. Inside the "square brackets" we write the position/index of the character required.
```
s4 = "Python"
len(s4)
6

#Indexing
s4[0]
'P'
s4[1]
'y'
s4[2]
't'
s4[3]
'h'
s4[4]
'o'
s4[5]
'n'
```

```
There is no index after 'n'.
What if we try to index the position/index which doesn't exist?
If we try to fetch s4[6] - It should throw an Index Error.
s4[6]
Traceback (most recent call last):
  File "<pyshell#35>", line 1, in <module>
    s4[6]
IndexError: string index out of range
```

The range for the string "Python" is 0 to 5.
How do we know the range? - Its straight forward - len(s4)
What is the last index of s4? - Its 5 [0,1,2,3,4,5]
Always remember, the last index of the string is **len-1**, because its starts the count from 0.

```
s1 = "Hello World"
s1
'Hello World'
len(s1)
11
s1[10]
'd'
```

Instead of trying the find the last index by this len-1, there is another way we can find the last index
Example - "Hello World"
```
 H   e   l  l  o     W  o  r  l  d
 0   1   2  3  4  5  6  7  8  9  10
-11 -10 -9 -8 -7 -6 -5 -4 -3 -2  -1
```

1. From 0 to 10 -> Its called "Positive Indexing" -> It basically starts form Left to Right
2. From -1 to -11 -> Its called "Negative Indexing" -> It basically starts form the last character starting from -1 [starts from Right to Left]
	1. Negative Indexing doesn't starts from 0, rather its starts from -1 from the right side and goes till -11 on the left side.
	2. Now if we want to fetch the last character of the string, instead of doing "len - 1", simply we can perform s1[-1]

```
s2
'We are learning Python'
type(s2)
<class 'str'>

s2
'We are learning Python'

s2[-1]
'n'
s2[-2]
'o'
```

We understand that there are "Positive" & "Negative" index/positions of strings in Python.
The Positive Indexing starts from Left to Right from 0 to n-1
The Negative Indexing starts from Right to Left from -1 to -n

---

**Joining of Strings Together**

1. Lets say we have 2 strings
	1. s1 & s2
	2. s1 = "Hello World"
	3. s2 = "We are learning Python"
		1. Joining of strings is done by "+" operator [ s1 + s2 ]
			1. s1 + s2
				1. 'Hello WorldWe are learning Python'
			2. One thing we can note here is that there is "no space"/"no gap" between the 1st string and the 2nd string.
		2. If we want to add a space in the middle
			1. s1 + ' ' + s2
				1. Hello World We are learning Python'
2. So, this is called joining/concatenation of the strings

```
# Joining of 2 strings

s1
'Hello World'
s2
'We are learning Python'
s1 + s2
'Hello WorldWe are learning Python'
s1 + '' + s2
'Hello WorldWe are learning Python'
s1 + ' ' + s2
'Hello World We are learning Python'
```

----
