
In this section, we shall look at mutability and immutability
Till now, we have seen data-types like Strings, Booleans, Integers, Floats, Lists & Tuples
Mutability is related to the data-types

Mutability is the ability of a value/data to be modified/changed
Immutability is the inability of a value/data to be modified/changed

We saw some examples on list where we append/extend/insert/remove/sort & reverse functions, wherein the existing list was getting changed

On the other hand, we didn't see any function that changes the string or the tuple.
So Strings & Tuples have the inability of a value/data to be changed/modified.

Lists are Mutable -> The value/data can be changed/modified
Strings & Tuples are Immutable-> The value/data cannot be changed/modified

Examples- 

1. String
	1. s1 = "Python is fun"
	2. s2 = s1.replace("Python", "Java")
	3. print(s1)
		1. "Python is fun"
	4. Replace function doesn't change/modify the existing string
		1. Rather it returns a new string, which we can store it in new variable called s2 and print s2
	5. print(s2)
		1. "Java is fun"
	6. So, the replacement is happening and its giving a new string to us. The existing string is not getting modified
		1. The existing string is untouched hence creating a new variable

**Basically Strings do not change their state after they are created - This is called Immutability**
**The State of the variable isn't changed**

```
# Mutability & Immutability  
# Lists are Mutable  
# Strings & Tuples are Immutable  
  
s1 = "Python is Fun"  
s2 = s1.replace("Python", "Fun")  
print(s1)  
print(s2)

Output Response -
Python is Fun
Fun is Fun
```

---

2. Tuples
	1. t1 = ("Mango", "Orange", "Apple")
	2. t1.append("Banana")
	3. print(t1)
		1. It will throw an error saying tuple object has no attribute 'append'
		2. This is because tuple and string doesn't support append function.

```
# tuples  
t1 = ("Mango", "Orange", "Apple")  
# t1.append("Banana")  
print(t1)

Ouput Response - 
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\ListsAreMutable-TuplesAreNot.py", line 13, in <module>
    t1.append("Banana")
    ^^^^^^^^^
AttributeError: 'tuple' object has no attribute 'append'
```


3. Lists 
	1. Wherein if we try to perform the same operation in Lists, it works because list supports the append function [Since Lists are mutable, it supports all functions which acts as modifying/changing the list]
	2. l1 = ["Mango","Orange","Apple"]
	3. l1.append("Banana")
	4. print(l1)
		1. ["Mango", "Orange", "Apple", "Banana"]

Lists are mutable data-types
Lists can change its state after creation

```
# lists  
l1 = ["Mango", "Orange", "Apple"]  
l1.append("Banana")  
print(l1)

Output Response - 
['Mango', 'Orange', 'Apple', 'Banana']
```


---
------


Another thing about mutability we have to understand is after the modification is done, the memory address of the list should be same
Its not re-assignment.

```
# lists  
l1 = ["Mango", "Orange", "Apple"] 
print(l1)
print(f"ID of L1 before the change is done : {id(l1)}")  
l1.append("Banana")  
print(l1)  
print(f"ID of L1 after the change is done : {id(l1)}")

Output Response -
['Mango', 'Orange', 'Apple']
ID of L1 before the change is done : 2064277943680
['Mango', 'Orange', 'Apple', 'Banana']
ID of L1 after the change is done : 2064277943680
```

The memory address remain the same and we confirm that Lists are mutable
The state is not changed. The existing list is being modified.

---
---

There is another way with which we change lists or mutable data-types in Python is by changing the value of a particular index (changing the value by using a particular index)
This is also considered as mutability since we are modifying the list
If a data-type is able to change the state of its own without changing address of itself is called mutability

```
# mutability examples  
l2 = ["Mango", "Orange", "Aple"]  
print(l2)  
print(f"ID of L2 before the change is done : {id(l2)}")  
l2[-1] = "Apple"  
print(l2)  
print(f"ID of L2 after the change is done : {id(l2)}")

Output Response - 
['Mango', 'Orange', 'Aple']
ID of L2 before the change is done : 1358452355648
['Mango', 'Orange', 'Apple']
ID of L2 after the change is done : 1358452355648
```


Tuples & Strings cannot do this since they are immutable.

Tuples -
```
# mutability examples with tuples - not possible  
fruits = ("apple", "banana", "chery")  
print(fruits)  
fruits[-1] = "cherry"  
print(fruits)

Output Response -
('apple', 'banana', 'chery')
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\ListsAreMutable-TuplesAreNot.py", line 35, in <module>
    fruits[-1] = "cherry"
    ~~~~~~^^^^
TypeError: 'tuple' object does not support item assignment
```

Strings
```
# mutability examples with strings - not possible  
s2 = "Python is Fun"  
print(s2)  
s2[0] = "J"  
print(s2)

Output Response -
Python is Fun
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\ListsAreMutable-TuplesAreNot.py", line 41, in <module>
    s2[0] = "J"
    ~~^^^
TypeError: 'str' object does not support item assignment
```

----
---


