
- In this section, we shall discuss about a module in python called **"Random"**
- What are modules?
	- Modules in Python are nothing but python files that have some python code written in it.
	- We can create our own modules by writing some some programs and saving them as .py files and using them in another file
	- We have in-built modules present in python as well.
	- So when we install python, python provides us certain kind of functions like print function, id function, etc.. -> These are part of the module which is pre-imported.
		- Since we are using them without doing any extra import.
	- But there are few functions which are part of different file or module that needs to be imported - Thats where these modules needs to be imported using the import keyword.
	- So, for the modules which are not part of the pre-imported modules, we need to 1st import them using the import keyword and then use the functions of those modules.
	- This section, we shall look at random module.


1. Random Function
	1. print(random.random())
		1. 0.7580556387423404
	2. The random function return the random value between 0.0 to 1.0
	3. But 1.0 value will be excluded
2. Random Function - randInt(a, b)
	1. print(random.randInt(0,10))
		1. 4
	2. The random module's randInt() function return the random integer between 0 to 10
	3. Both the  0 and 10 will be included
3. There are couple of functions that we can apply on a sequence of list
	1. nums = [10, 3, 7, 2, 6, 1, 0]
		1. choice(sequence) => returns a random item from the sequence
		2. The random module's choice(sequence) return the random item/element from the list/tuple or any other sequence data-type
			1. It will return one of the entries from the list/tuple or any other sequence data-type
4. There is another function called Shuffle
	1. It also takes a sequence like a list as an argument and it returns the elements shuffled in random order also as an output of the shuffle function, the list itself will change
	2. It returns NONE -> Its actually the output of the print(random.shuffle())
		1. Basically random.shuffle doesn't print anything
	3. Shuffle can be used in the card games


```
import random  
  
# random() -> returns random float between 0.0 and 1.0(excluded)  
print("Random Function")  
print(random.random())  
  
# randint(a, b) -> returns random integer value between a and b (both included)  
print(f"\nRandInt Function")  
print(random.randint(0,10))  
  
# choice(sequence) -> returns a random item from the sequence  
print(f"\nChoice Function")  
nums = [10, 3, 7, 2, 6, 1, 0]  
print(random.choice(nums))  
fruits = ['apple', 'banana', 'orange']  
print(random.choice(fruits))  
  
# shuffle(sequence) -> returns the elements shuffled in random order  
print(f"\nShuffle Function")  
fruitsAgain = ['mango','pineapple','mango', 'strawberry']  
random.shuffle(fruitsAgain)  
print(fruitsAgain)

Output Response -
Random Function
0.8384655245841779

RandInt Function
9

Choice Function
2
banana

Shuffle Function
['mango', 'strawberry', 'mango', 'pineapple']
```


---
---
