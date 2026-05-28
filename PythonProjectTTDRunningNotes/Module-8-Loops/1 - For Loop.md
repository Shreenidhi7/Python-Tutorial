
- What is Loop?
	- As the name suggests, loop is something which goes repeatedly.
	- Doing same thing again and again.
	- So anytime, we need to do a repetition of work
	- In terms of programming, anytime we have to repeat a block of program, any number of times we will use loop
	- Example - Doing some work in Loop
		- Listening to songs - same song in a loop
	- There are 2 types of loops in python.
		- For Loop
		- While Loop

1. For Loop
	1. For Loop in python basically is an iterator based loop which steps through the items of a collection like lists, tuples, sets, dictionaries, strings and executes a block of code repeatedly for a number of times equal to the items/elements of the collection.
		1. Lets say there are 5 elements/items in the collection, For Loop will run 5 times
	2. Its a Definite Loop - Its a Finite Loop
		1. We know how many times the loop will execute.
	3. Syntax -
		1. keyword = for
		2. variable = var
		3. collection = sequence
	4. for var in sequence:
		1. statement1
		2. statement2
		3. ...
		4. ...
		5. statementN
	5. The syntax means for each element in the sequence, the value will be stored in the variable "var" and it will be executing all the statements in the block.


- Example - When we want to print all the values from a list.
	- Here lets say we have small list which has 4 items in it.
		- percents = [85.5, 81.0, 86.0, 83.5]
			- print(percents[0])  
			- print(percents[1])  
			- print(percents[2])  
			- print(percents[3])
	- This is a normal way to print/fetch each item from the list.
	- Here we know the length of the items of the list and we can fetch that easily by extracting all the items individually
- But what if the list is huge having thousands of items/elements in it.
- Is it possible to print all of the elements one by one?
	- There won't be any problem in doing it, but it would need more manual effort and its a tedious work and not a good way of writing program.
- So therein the concept of FOR LOOP will come into picture
	- Since For Loop runs on a collection
	- Each repetition is called an iteration
	- So in 1st iteration, the 1st element of the percents list gets assigned to the variable called p.
		- p becomes 85.5
		- p becomes 81.0 in the next iteration - python overwrites this value
		- p becomes 86.0 in the next iteration - python overwrites this value
		- p becomes 83.5 in the next iteration - python overwrites this value
	- After printing the last value, it again goes back to the for loop and looks for any next element in the list. If there is no next element in the list, python sees that percents elements are exhausted and there is no element left in the list.
		- It exists from the loop and goes out of the loop.
	- It has run 4 times which is nothing but the length of the list.
- The Loop runs maximum to the length of the list.

```
percents = [85.5, 81.0, 86.0, 83.5]  
print(percents[0])  
print(percents[1])  
print(percents[2])  
print(percents[3])

Output Response -
85.5
81.0
86.0
83.5
```

```
percents = [85.5, 81.0, 86.0, 83.5]
for p in percents:  
    print(p)
    
Output Response -
85.5
81.0
86.0
83.5
```


---
---

