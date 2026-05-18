
- Sets are another data-type like how have see Strings, Lists & Tuples
- Sets are also non-sequential collection of elements or items
- In Lists are Tuples, we saw that both Lists & Tuples are in sequence
- Important - Sets are non-sequential collection.
	- It means that we cannot have indexing in sets
- Sets are created by writing comma separated elements/items enclosed within curly brackets
	- Square Brackets are Lists - []
	- Parenthesis or Round Brackets are Tuples - ()
	- Curly Brackets are Sets - {}

```
# Sets are non-sequential collection of items  
# comma separated elements enclosed within {}  
  
set1 = {10, "Python", 2.5}  
print(set1)  
print(type(set1))

Output Response -
{10, 2.5, 'Python'}
<class 'set'>
```


- Indexing is not allowed in Sets
	- They are non-sequential (They are not in any order or sequence)

```
# indexing - not allowed in sets  
set1 = {10, "Python", 2.5}
print(set1[0])

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\4-IntroductionToSets.py", line 9, in <module>
    print(set1[0])
          ~~~~^^^
TypeError: 'set' object is not subscriptable
```

- Since indexing is not allowed, Slicing operation is also not allowed on Sets

- Finding length of the set.
```
# Length of the set
set1 = {10, "Python", 2.5} 
print(len(set1))

Output Response -
3
```

---

When we have lists and tuples
- Lists are collection of elements/items enclosed within square brackets
- Tuples are collection of elements/items enclosed within round brackets
- The difference between Lists and Tuples are
	- Lists are mutable
	- Tuples are immutable

When we have Lists and Tuples data-types/data structures then why do we need Sets?
- Sets have another feature that is different from Lists and Tuples

Question
- Can we have duplicate elements/items in a list and tuple?
Answer
- Yes, we can have duplicate elements in a list and a tuple.

This is where the difference b/w a set and a list and a tuple comes into picture.
Sets are data structures which do not have duplicates in them [Sets do not allow duplicate elements or same elements] - It means that if there are duplicates inside the set, then only one instance will be considered.

```
# sets do not allow duplicate elements  
l1 = [10,2.5,10,30,10]  
print(l1, type(l1))  
set1 = {10, 2.5, 10, 30, 10}  
print(set1, type(set1))

Output Response -
[10, 2.5, 10, 30, 10] <class 'list'>
{10, 2.5, 30} <class 'set'>
```

There would be no error when the set have duplicate elements/items inside them, but if we observe the output carefully, we can see that the duplicate elements 
In the above example, in a set, we have 10 -> 3 times in the set,  but when printed as the output 10 is printed only once
- Even if while creating set, if we have duplicate elements in them, only one occurrence of that element will be stored in a set. Others will be discarded because duplicates are not allowed in a set.

Major difference b/w Sets and Lists/Tuples
- Sets cannot have duplicates in them
- Lists/Tuples can have duplicates in them

----

- What is the use case/usage of Sets? When do we use Sets?
	- Think of an example where Tuples/Lists will not be used/cannot be used to store something
- Anything that is unique should be stored in Sets.
	- Example - Any Identification Number
		- Every individual of every country will have some identity
			- Example - Passport
- Sets can be used to store these kind of data
	- Passport number of all the individuals of a country or certain area

---


