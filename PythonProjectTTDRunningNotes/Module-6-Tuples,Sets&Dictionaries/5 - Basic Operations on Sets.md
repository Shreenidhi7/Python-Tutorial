
- In this section, we shall discuss on the basic operations on the sets

Membership Operators [ in and not in ]
- The "in" operator checks and gives us True if any element/item "present" in the List/Tuple and in Sets
- The "not in" operator checks and gives us False if any element/item "not present" in the List/Tuple and in Sets

```
nums = {1, 3, 2 , 0, -1}  
  
# membership operator - in and not in  
print(f"membership operators - in and not in")  

print(0 in nums)  
print(10 not in nums)  
  
print(5 in nums)  
print(1 not in nums)

Output Response -
membership operators - in and not in
True
True
False
False
```

----

- We already know that we cannot do indexing and slicing on sets. So what else can we do in sets?
	- Can we perform concatenation on sets?
- No, we cannot perform concatenation operation on sets
```
# concatenation operation - not possible on sets  
print(f"Concatnation Operation on Sets - Not Possible")  
num1 = {1, 2, 3}  
num2 = {4, 5, 6}  
print(num1 + num2)

Output Response -
Concatnation Operation on Sets - Not Possible
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\5-BasicOperationsOnSets.py", line 16, in <module>
    print(num1 + num2)
          ~~~~~^~~~~~
TypeError: unsupported operand type(s) for +: 'set' and 'set'
```


Repeating Sets?
- Not Supported
- Repetition could be done on Lists/Tuples & Strings but not in Sets
```
# repetition operation - not possible on sets  
print(f"Repetition Operation on Sets - Not Possible")  
print(num1 * 3)

Output Response -
Repetition Operation on Sets - Not Possible
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\5-BasicOperationsOnSets.py", line 20, in <module>
    print(num1 * 3)
          ~~~~~^~~
TypeError: unsupported operand type(s) for *: 'set' and 'int'
```

---

Converting Tuples to Sets
- Its possible using Typecasting.
```
# converting tuple to set  
print(f"Converting Type to Sets")  
weekdays = ("mon", "tue", "wed", "thur", "fri", "sat", "sun")  
weekdays_set = set(weekdays)  
print(weekdays_set, type(weekdays_set))

Output Response -
Converting Type to Sets
{'tue', 'wed', 'sun', 'sat', 'thur', 'mon', 'fri'} <class 'set'>
```

The order in which they were already created inside the tuple, the same order is not followed
Because Sets are Unordered/Non-Sequential data-type.
When we re-run/re-execute the same program, we can observe that the output, we see its a different order again
[ The order in which the tuples are created and if we are converting that into a set and storing them, the order will not be there (Because sets donot have any order in them)]
So, this proves that Sets are Non-Sequential/Unordered data-structure.

Similarly, it could be list and we can convert that list into a set.

---

What was the major difference that we saw b/w Tuples and Lists?
- Mutability
	- Lists are mutable
		- We can change/modify the elements of the list
	- Tuples are non-mutable
		- We cannot change/modify the elements of the tuple

Are Sets Mutable or Immutable/
- Sets are Mutable
	- We can change/modify the elements of the sets
	- But there are certain clause to it.

We cannot perform set[0] -> Because we cannot have indexing in Sets
- There is no position/index in Sets
There are other ways to check the variable/datatype is mutable or not.

In Lists, we have seen certain functions/methods using which we can add/remove elements from the list. [Append,Extend,Remove,Pop]

Similar to that, Sets also have certain functions
1. Add
	1. As the name suggests - it adds elements to the set.
	2. It doesn't matter where the element gets added because sets are un-ordered data-type/there is no sequence of elements inside the set.
	3. Assume that set1 is like a bowl and have some balls in it.
		1. When we use set1.add -> the bowl gets added with more balls
	4. The reason to consider it as bag/bowl is that we can put things randomly
2. Remove
	1. Remove function deletes an element/item of a set if it is present.
	2. Also it is a permanent deletion from the sets itself.

```
# Are Sets Mutable or Immutable?  
print(f"\nAre Sets Mutable or Immutable?")  

set1 = {2, 0, -1}  
print(f"Before the add function : {set1} and the type of the variable is : {type(set1)}")  

# add()  
set1.add(5)  
print(f"After the add function : {set1} and the type of the variable is : {type(set1)}")

# remove()  
set1.remove(5)  
print(f"After the remove function : {set1} and the type of the variable is : {type(set1)}")

Output Response -
Are Sets Mutable or Immutable?
Before the add function : {0, 2, -1} and the type of the variable is : <class 'set'>
After the add function : {0, 2, 5, -1} and the type of the variable is : <class 'set'>
After the remove function : {0, 2, -1} and the type of the variable is : <class 'set'>

```


If the element/item is not present in the set, then if we perform set1.remove(10), then there would be a function error
```
set1 = {2, 0, -1}  
print(f"Before the add function : {set1} and the type of the variable is : {type(set1)}")

set1.remove(10)  
print(f"After the remove function : {set1} and the type of the variable is : {type(set1)}")

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\5-BasicOperationsOnSets.py", line 36, in <module>
    set1.remove(10)
    ~~~~~~~~~~~^^^^
KeyError: 10
```

KeyError: 10 => It means that the element 10 is not present in the set to be removed.
If something is not there, we cannot remove it. So Python gives an error

- The elements of the set are set1 = {2, 0, -1}
- If i add new element/item to the set set1.add(5)
	- Its gets added
- Now, what will happen if we try to add new element/item to the set [the same number which already exists in the set]
	- We know that Sets do not allow duplicate elements
	- Once run, there won't be any error and since duplicates are not allowed in a set, there won't be any difference in the set

```
# add again()  
print(f"set1 : {set1}")  
set1.add(2)  
print(f"set1 after adding 2 : {set1}")

Output Response -
set1 : {0, 2, -1}
set1 after adding 2 : {0, 2, -1}3
```

---

For Removing/Deleting elements from the set, there is another function called "Discard"
- This Discard function actually deletes the element from the set.

```
# discard()  
print(f"set1 : {set1}")  
set1.discard(2)  
print(f"set1 after discarding : {set1}")
set1.discard(10)  
print(f"set1 after discarding the element not present in set : {set1}")

Output Response - 
set1 : {0, 2, -1}
set1 after discarding : {0, -1}
set1 after discarding the element not present in set : {0, -1}
```

If we have remove function, then why do we have discard function?
- Remove
	- It deletes an element/items if that element is present in the set
	- It gives an error if the element is not present in the set
- Discard
	- It deletes an element/items if that element is present in the set
	- It doesn't give an error if the element is not present in the set

	If we want to avoid errors, if we are not sure if a particular element is there or not while deleting elements from a set, its better to used Discard

-----------

- Sets are similar to the Mathematical Sets
- Mathematics has some set theory
	- Union of Sets
	- Intersection of Sets
	- Difference b/w Sets etc
- Python Sets and Mathematical Sets are similar to each other.
- Python supports the Mathematical Set Operation on the Set data-type

