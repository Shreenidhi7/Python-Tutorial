

List is a data structure or a data type in which we can store collection of data.
- It means any type of data that can be stored within a single variable or single data type.

Lets say we have some information of some student stored in 3 variables.
- name = "Shree"
- age = 29
- percent = 85.5
Here we have stored 3 pieces of information that we have stored in 3 different variables.

Question
- Instead of doing this, can we store this into a single variable or a single collection of data so that it represents one student data?
Answer
- Yes, its possible
- Lists are collection of items or data within them, which can store any type of data
- In the above example of Shree, we can store all 3 information of this student together in the single group of data which is list.

List can be created with a pair of square brackets. The data which we want to store in a list will be enclosed within a pair of square brackets and the data will be comma separated within each other.
- student = ["Shree", 29, 85.5]
	- Now name,age,percent data is associated with a single student.
- Lists are in general created when we want to club the data together in a single entity
- The variable student is a list.
	- How to verify student is a list?
		- print(type(student))
```
student = ["Shree", 29, 85.5]  
print(student)  
print(type(student))

Output Response - 
['Shree', 29, 85.5]
<class 'list'>
```

One thing we understood about list is that it can contain multiple values/data of different/any datatype.
When we created a list for the student, we added a "String", "Integer" and "Float"
Any datatype is allowed as an item or an element of a list.

String is collection/group/sequence of characters
Similarly Lists are collection/group/sequence of any data

Lists store the value/data in the ordered way.
- Example - 
	- daysOfWeek = ["Mon", "Tue", "Wed", "Thru", "Fri", "Sat", "Sun"]
		- All these values/data are in the order.
- Similar to Strings, we have positioning/indexing in lists.
- Indexing works exactly similar to Strings.
- The 1st item/element have the index 0 [1st index element starts with 0]
- Each element have their own index.
	- Also we can observe that it is in the sequence/order
- Every data will be associated with an index in an ordered manner.

If Lists have index, then obviously we can do indexing and fetch an element of a list like how we fetch a character of a string by using indexing.
Also we have both positive and negative indexing.
- Positive Indexing - Its starts from the left side with 0, 1, 2, 3 and goes on until the length of the list.
- Negative Indexing - It starts from the right side with -1, -2, -3 and goes on until the length of the list.
What is Length of the List?
- Length of the list is nothing but the number of items or elements in the list.
How to find the length of the list?
- Using the Len function.

```
name = "Shree"  
age = 29  
percent = 85.5  
  
student = ["Shree", 29, 85.5]  
print(student)  
print(type(student))  
  
daysOfWeek = ["Mon", "Tue", "Wed", "Thru", "Fri", "Sat", "Sun"]  
print(daysOfWeek[0])  
print(daysOfWeek[4])  
  
# Positive Indexing  
print(f'Last day of the week is {daysOfWeek[6]}')  
# Negative Indexing  
print(f"Last day of the week is {daysOfWeek[-1]}")  
  
# Length of the List => The number of items/elements in the list  
print(f"Length of the list is {len(daysOfWeek)}")

Output Response - 
['Shree', 29, 85.5]
<class 'list'>
Mon
Fri
Last day of the week is Sun
Last day of the week is Sun
Length of the list is 7
```

Question
- What if we perform print(daysOfWeek[8])
	- We are trying to fetch the element or an item which is at the the 8th index.
Answer
- The list variable daysOfWeek has only 6 indexes starting from 0
	- Mon - 0
	- Tue - 1
	- Wed - 2
	- Thru - 3
	- Fri - 4
	- Sat - 5
	- Sun - 6
- We don't have anything at the 7th index or the 8th index.
- So if we try to fetch the values from the index which doesn't exist, then we get an Index error saying "Index out of range"
	- It means that the index we are trying to use to fetch the element of this daysOfWeek is out of the list.
- The range of the index of this list is 0 to 6 because the length is 7
	- If we try to use an index which is not part of that range, we shall get an index error

```
# Index out of range  
print(daysOfWeek[8])

Output Response - 
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Lists in Python\ListsIntroduction.py", line 22, in <module>
    print(daysOfWeek[8])
          ~~~~~~~~~~^^^
IndexError: list index out of range
```

----
