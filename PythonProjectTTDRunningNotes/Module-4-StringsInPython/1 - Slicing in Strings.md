
This section, we shall discuss about slicing in strings.
Before that we shall have a quick recap on strings.

```
s1 = "Hello World"  
print(s1)  
  
# Length of the String  
print(len(s1))  
  
# Indexing in Python for Strings  
print("First Character "+s1[0])  
print("Last Character "+s1[-1])

Output - 
Hello World
11
First Character H
Last Character d
```

---

What is Slicing?
- Slicing is the technique where it enables a programmer to access/fetch a part of the string.
- The output will be a substring of the string.
	- Real Time Example - Its like a cake wherein you want to slice a cake and take the part that we want eat.
- Slicing can we used with Strings, Lists, Tuples etc...
- Example - With the word "Hello World"
	- Indexing will fetch a particular character [One character at a time]
	- Slicing on an other hand, can fetch an entire word/part of the word for us.
		- Example - "Python is Fun"
			- Here if want to fetch the word "Python" - This can be possible with slicing.

---

Syntax of Index
- string[index]

---

Syntax of Slicing
- string[start:end:step]
	- In square brackets, we write **starting index** : **ending/stop index** : **step in which we want to perform slice**
- start index - Its nothing but starting index at which the slicing operation starts
	- When we cut a cake, we start from a position - that position is called start index
- end index - Its the ending index/stopping index at which the slicing operation stops/ends (excluded)
	- From slicing, the ending index is excluded
- step - Its an integer that specifies the step for the slicing [increment/decrement]

Lets take an example to understand the slicing operation.
```
s1 = "Hello World"  
print(s1)
print(s1[2:7:1])

Output - 
Hello World
llo W
```

```
H e l l o   W o r l d
0 1 2 3 4 5 6 7 8 9 10
```

- Start index is 2 -> It means it will start at 2nd index
	- l
- End index is 7 -> It means it will end at the 7th index [also its been mentioned that it is excluded]
	- It means that the 7th index will not be included in the output [In our case its "o"]
- Step index is 1 -> It means that after the slicing has started, it has to slice 1 step at a time [its like climbing the stairs 1 step at a time(1st step,2nd step,3rd step...)]
	- So, here the slicing has started at "l", and the step is 1, then that means the next step is "l"
- Final Output -> l l o W
	- It will start at 2nd index included
	- It will take 1 step at a time
	- It will end at 6th index [because the last index is excluded by default]


---

Lets take an another example to understand the slicing operation.
```
s1 = "Hello World"  
print(s1)
print(s1[2:9:2])

Output - 
Hello World
l o W r
```

```
H e l l o   W o r l d
0 1 2 3 4 5 6 7 8 9 10
```

- Start index is 2 -> It means it will start at 2nd index
	- l
- End index is 9 -> It means it will end at the 9th index [also its been mentioned that it is excluded]
	- It means that the 9th index will not be included in the output [In our case its "l"]
- Step index is 2 -> It means that after the slicing has started, it has to slice 2 step at a time [its like climbing the stairs 2 step at a time(2nd step,4th step,6th step...)]
	- So, here the slicing has started at "l", and the step is 1, then that means the next step is "o"
- Final Output -> l o W r
	- It will start at 2nd index included
	- It will take 2 step at a time
	- It will end at 8th index [because the last index is excluded by default]


----

Lets take an another example to understand the slicing operation.
```
s1 = "Hello World"  
print(s1)
print(s1[1:12:3])

Output - 
Hello World
e o o d
```

```
H e l l o   W o r l d
0 1 2 3 4 5 6 7 8 9 10
```

- Start index is 1 -> It means it will start at 1st index
	- e
- End index is 12 -> It means it will end at the 11th index [also its been mentioned that it is excluded]
	- It means that the 12th index will not be included in the output [In our case its " "] (no character available)
- Step index is 3 -> It means that after the slicing has started, it has to slice 3 step at a time [its like climbing the stairs 3 step at a time(3rd step,6th step,9th step...)]
	- So, here the slicing has started at "e", and the step is 3, then that means the next step is "o"
- Final Output -> e o o d
	- It will start at 1st index included
	- It will take 3 step at a time
	- It will end at 10th index [because the last index is excluded by default]

Question
- Since the word "Hello World" only have 11 characters in it, What happens if we provide the last/stop index as 12? Will it fail during the execution? Will it throw an error?
Answer
- Yes, we don't have the 12th index.
	- If we just do string[index of 12] -> this throws me an error.
- When we write the index in slicing when it is more than last index [in our case the last index is 10] - Python will consider the character which are present till the last step index, after the indexing is not considered.

One more important thing
- Once sliced, output will always be string.

----

```
s1 = "Hello World"  
print(s1)  
   
print(s1[2:7:1])  
print(type(s1))

print(s1[2:9:2])  
print(type(s1))  

print(s1[1:12:3])  
print(type(s1))

Output - 
Hello World

llo W
<class 'str'>

loWr
<class 'str'>

eood
<class 'str'>
```


----
