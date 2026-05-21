
- In this section, we shall discuss about something called Frozen Sets
	- Sets are collection of elements stored in curly brackets in a comma separated way.
	- We can store unique elements in a Set [There shouldn't be any duplicate elements in the set]
	- We can add/remove elements from the sets, because they are mutable and we can perform certain operations like union, intersection and difference - This proves that Sets are Mutable

This time, we shall discuss about Frozen Sets and how they are different from Sets.
- Frozen Sets are Immutable Sets
	-  There might be certain scenarios where we want to have unique elements but those should not be changed as well
		- This case we can use Frozen Sets
- Normal Sets can be used to store non-duplicate or unique elements also should be able to add/remove elements if required.
- In Frozen Sets - An Extra feature comes into picture [that is immutability] wherein we shouldn't be able to change/modify the state of the set.
	- Also FrozenSets are created with the pre-fix frozenset({})

```
# Normal Set - Mutable [Can change the state of the set]  
s1 = {1, 2, 4, 0}  
s1.add(3)  
print(s1)  
  
# Frozen Set - Immutable [Cannot change the state of the set]  
fs1 = frozenset({10, 20, 30})  
print(fs1, type(fs1))

Output Response -
{0, 1, 2, 3, 4}
frozenset({10, 20, 30}) <class 'frozenset'>
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\7-FrozenSets.py", line 10, in <module>
    fs1.add(10)
    ^^^^^^^
AttributeError: 'frozenset' object has no attribute 'add'
```


---

If we try to add an element to the frozenset, lets check what will happen
Any operation that changes the state of the data/set will not be allowed in FrozenSet
```
# Frozen Set - Immutable [Cannot change the state of the set]  
fs1 = frozenset({10, 20, 30})  
print(fs1, type(fs1))  
  
fs1.add(10)  
print(fs1, type(fs1))

Output Response -
frozenset({10, 20, 30}) <class 'frozenset'>
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\7-FrozenSets.py", line 10, in <module>
    fs1.add(10)
    ^^^^^^^
AttributeError: 'frozenset' object has no attribute 'add'
```

---

- We can have Union, Intersection and Difference in FrozenSets as well.
	- This is because when we perform the above operation, there would be a new set that would be created and the final output will be stored in that new set.

```
  
# Frozen Set - Immutable [Cannot change the state of the set]  
fs1 = frozenset({10, 20, 30})  
print(fs1, type(fs1))  
  
fs2 = frozenset({10, 50, 100, 200})  
print(fs2, type(fs2))  
  
#Intersection  
intersection = fs1.intersection(fs2)  
print(f"intersection : {intersection}, type => {type(intersection)}")  
  
#Union  
union = fs1.union(fs2)  
print(f"union : {union}, type =>  {type(union)}")  
  
difference = fs1.difference(fs2)  
print(f"difference : {difference}, type => {type(difference)}")

Output Response -
frozenset({10, 20, 30}) <class 'frozenset'>
frozenset({100, 10, 50, 200}) <class 'frozenset'>
intersection : frozenset({10}), type => <class 'frozenset'>
union : frozenset({50, 20, 100, 200, 10, 30}), type =>  <class 'frozenset'>
difference : frozenset({20, 30}), type => <class 'frozenset'>
```