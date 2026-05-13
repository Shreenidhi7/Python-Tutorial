
In this section, we shall get introduced with a new data type called Tuple
Tuple is very similar to List
Tuples are also comma-separated elements enclosed within brackets
In List, we enclose the elements/items in Square Brackets []
But in Tuples, we write elements/items in Round Brackets or Parenthesis.
- Example => (item1, item2, ...)
Bracket is the difference between list and a tuple while creation
Its basically sequence or group of sequence of items as a collection

List -> A sequence of elements or items in a collection, comma-separated enclose with square brackets
Tuple -> A sequence of elements or items in a collection, comma-separated enclosed with round brackets

---

List and Tuple both can store data of any data-type.
We have lists already, Why do we need Tuples?
What is the major difference between List and Tuple?

In List, we use append, remove, extend, insert, pop etc functions [
( Append/Extend/Insert - These functions are for adding elements from a list )
( Remove/Pop - These functions are for removing elements from a list )
(Reverse - To reverse the elements of the list)
(Sort - To sort the elements ascending/descending of the list)
All these operations are modifications on the list

This is where the difference comes into the picture b/w list and tuple.
We donot have any of these functions in tuple
We cannot modify the tuple
(We can add/extend/delete any elements from the tuple)
When we create a tuple, the elements are fixed

---

Where do we use list and tuple?
1. Tuple - 
	1. Storing months of the year.
		1. Since there is no possibility of changing [Ideally we wont be adding the 13th month for the year (12 months per year is fixed in calender)]
	2. Similarly days of the week
		1. Monday to Friday - Weekdays
		2. Saturday and Sunday - Weekends
	3. If somebody asks you to create a collection of weekdays
		1. Tuples can be used to write/create those elements where we do not modify something
2. Lists
	1. Its used when we need to modify or there is scope of modification in the list
	2. Example - Recipe of some delicious food
		1. Lets say we forgot to add some ingredient - So we add/modify/delete the element/item at the first/middle/last of the list
	3. Example - List of Student Name/Student Roll Numbers
		1. We shouldn't store these in a Tuple, because we cannot add a new student if he gets enrolled

---

Few Basic Examples

```
# Tuple  
# (item1, item2, ...)  
# sequence of items as a collection  
  
t1 = ("Python", 10, 1.5, True, [1,2,4], (10,20))  
print(t1)  
print(type(t1))  
# length of the tuple  
print(len(t1))  
# accessing the items of the tuple - index  
print(t1[0])  
print(t1[-1])  
# slicing the items of the tuple  
print(t1[1:5:1])

---
Output Response - 
('Python', 10, 1.5, True, [1, 2, 4], (10, 20))
<class 'tuple'>
6
Python
(10, 20)
(10, 1.5, True, [1, 2, 4])
```

---

Another way to create a tuple
- The parenthesis is optional
	- Even though we won't provide the round brackets it is considered as a tuple not as a list

```
# another way to create a tuple  
t2 = 10,20,30,40,50  
print(t2)  
print(type(t2))

Output Response -
(10, 20, 30, 40, 50)
<class 'tuple'>
```

----

Question
- Can we convert a list to a tuple?
Answer
- Yes, its possible.
	- Its typecasting to itself
- Typecasting doesn't mean that the existing value will change, it will give a new value

```
###############  
# converting list to a tuple  
l3 = [10,20,30,40,50]  
print(l3)  
print(type(l3))  
t3 = tuple(l3)  
print(t3)  
print(type(t3))

Output Response - 
[10, 20, 30, 40, 50]
<class 'list'>
(10, 20, 30, 40, 50)
<class 'tuple'>
```


----

Question
- Can a tuple be converted to list?
Answer
- Yes, its possible.
	- Its typecasting to itself
- Typecasting doesn't mean that the existing value will change, it will give a new value
	- But here we are just re-assigning the values to the fruits variable

```
# converting tuple to a list  
fruits = ("mango", "orange", "apple", "banana")  
print(fruits, type(fruits))  
  
fruits = list(fruits)  
print(fruitsList, type(fruitsList))

Output Response -
('mango', 'orange', 'apple', 'banana') <class 'tuple'>
['mango', 'orange', 'apple', 'banana'] <class 'list'>
```

---
We cannot do any append/remove operations on tuple, but we can type the tuple to list and then we can do all available list operations on the list.

---
---

