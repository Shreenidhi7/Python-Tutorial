
- In this section, we will continue with Dictionaries
- Here we shall work with keys and values of dictionaries and we will look at features of keys and values like how to fetch keys, how to fetch items and values of dictionary.

1. Types of Keys
	1. Not-Allowed Keys - List, Set, Dict
		1. Lists
			1. d1 = {[1,2,3] : 6, [1,2] : 3}
		2. Sets
			1. d1 = {{1,2,3}: 6, {1,2}: 3}
		3. Dictionaries
				1. d1 = {{'a':1,'b': 2} : 6}
	2. Allowed Keys - String, Integer, Float, Boolean, Tuple
		1. Strings
			1. d1 = {"Nine" : 9, "Four" : 4}
		2. Integers
			1. d1 = {1: True, 0: False}
		3. Floats
			1. d1 = {1.0: True, 0.0: False}
		4. Boolean
			1. d1 = {True: 1, False: 0}
		5. Tuple
			1. d1 = {(1,2,3): 6, (1,2): 3}

Question
- What is the relation between List, Set & Dictionary?
	- How they are different from String, Integer, Float, Boolean and Tuple?
Answer
- List, Set & Dictionary are mutable
	- We can change the state of the List, Set & Dictionary
- String & Tuple are Immutable [We cannot change the state of it]
	- Even Integer, Float and Boolean state cannot be changed. They can we re-assigned for sure but that's not mutability
	- They are all Immutable data-types

It means that keys of the dictionary can only be mutable data-type
Values can be any datatype

Value - List
```
# value = List  
student1 = {"id" : 1001, "name": "Shree", "marks" : [89.5, 71.5, 81.0]}  
print(student1)  
print(student1["name"])  
print(student1["marks"][2])

Output Response -
{'id': 1001, 'name': 'Shree', 'marks': [89.5, 71.5, 81.0]}
Shree
81.0
```

Value - Dictionary
```
# value = Dictionary  
student2 = {"id" : 1001, "name": "Shree", "marks" : {"english" :89.5, "maths" :71.5, "biology" :81.0}}  
print(student2)  
print(student2["name"])  
print(student2["marks"]["english"])

Output Response -
{'id': 1001, 'name': 'Shree', 'marks': {'english': 89.5, 'maths': 71.5, 'biology': 81.0}}
Shree
89.5
```

---
---

1. Functions to fetch Key & Values
	1. Fetch all the keys of the dictionary
		1. There is a function called keys() -> this will fetch only the keys of that dictionary
	2. Fetch all the values of the dictionary
		1. There is a function called values() -> this will fetch only the values of that dictionary
	3. Fetch both keys and values - the pair together
		1. There is a function called items() -> this will fetch the keys and items together of that dictionary

```
# fetch all the keys of the dictionary  
student2 = {"id" : 1001, "name": "Shree", "marks" : {"english" :89.5, "maths" :71.5, "biology" :81.0}}  
print(student2)  
print(student2.keys(), type(student2.keys()))  
  
# fetch all the values of the dictionary  
print(student2)  
print(student2.values(), type(student2.values()))

# fetch keys and value both as a pair together  
print(student2)  
print(student2.items(), type(student2.items()))

Output Response -
{'id': 1001, 'name': 'Shree', 'marks': {'english': 89.5, 'maths': 71.5, 'biology': 81.0}}
dict_keys(['id', 'name', 'marks']) <class 'dict_keys'>
{'id': 1001, 'name': 'Shree', 'marks': {'english': 89.5, 'maths': 71.5, 'biology': 81.0}}
dict_values([1001, 'Shree', {'english': 89.5, 'maths': 71.5, 'biology': 81.0}]) <class 'dict_values'>
{'id': 1001, 'name': 'Shree', 'marks': {'english': 89.5, 'maths': 71.5, 'biology': 81.0}}
dict_items([('id', 1001), ('name', 'Shree'), ('marks', {'english': 89.5, 'maths': 71.5, 'biology': 81.0})]) <class 'dict_items'>
```

Important - The items() returns the pair in the form of tuple not in a form of dictionary.
Each tuple is a key-value pair

---
---
