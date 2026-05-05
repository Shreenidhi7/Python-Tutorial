
1. Extend Function
	1. Extend function/method is similar to what insert and append does.
		1. Append and Insert basically add elements to the list.
			1. Append adds the element at the end of the list
			2. Insert adds at a particular index
	2. Extend basically adds the element at the end of the list, but what would be the difference b/w append and extend?
		1. Append function can add only one element at a time
		2. If we try to add multiple values at a time, it would throw a "Type Error"
			1. list.append() takes exactly one argument (2 given)
				1. It means append function takes only one element to be added in the list, but we have given 2 elements, which is wrong by the way
		3. In these situations, wherein we want to add multiple fruits to the fruits list [multiple elements to any list] we should be using "Extend" function
	3. In Extend function, we will not give comma seperated values, but we provide it in a list [list of values]
		1. ["orange","mango"]
		2. The extend function will add these 2 elements at the end of the list
		3. Important Note - It will not be adding this entire list as a single element, rather it adds "orange" as one element and "grapes" as another element
		4. If we see how many elements are in fruits lists before extend?
			1. Its 3
		5. If we see how many elements are in fruits lists after extend?
			1. Its 5

Append Function with Multiple Elements
```
fruits = ["apple", "banana", "cherry"]  
fruits.append("orange","mango")

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Lists in Python\ListOperations-In-Python-2.py", line 9, in <module>
    fruits.append("orange","mango")
    ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
TypeError: list.append() takes exactly one argument (2 given)
extend function
```

Extend Function with Multiple Elements
```
print("extend function")  
  
fruits = ["apple", "banana", "cherry"]  
print(f"the total number of fruits before the extend function is : {len(fruits)} and the fruits are {fruits}")  
fruits.extend(["orange","mango"])  
print(f"the total number of fruits after the extend function is : {len(fruits)} and the fruits are {fruits}")

Output Response - 
extend function
the total number of fruits before the extend function is : 3 and the fruits are ['apple', 'banana', 'cherry']
the total number of fruits after the extend function is : 5 and the fruits are ['apple', 'banana', 'cherry', 'orange', 'mango']
```

-----------

Question
- What if we use the extend method the below mentioned way
	- fruits.extend("Banana","Grapes")
Solution
- This also gives an error (type error) - similar to append function
```
# extend with multiple values  
fruits.extend("tomato", "pineapple")

Output Response - 
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Lists in Python\ListOperations-In-Python-2.py", line 15, in <module>
    fruits.extend("tomato", "pineapple")
    ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
TypeError: list.extend() takes exactly one argument (2 given)
```

----

Question
- What happens if we use append method the below mentioned way
	- fruits.append(["Banana","Grapes"])
Solution
- It actually doen't give an error. It works.
	- If we see the output, it has added a list inside the list.
```
# append with multiple values but in an array  
fruits.append(["tomato","pineapple"])  
print(fruits)
print(len(fruits))

Output Response - 
['apple', 'banana', 'cherry', 'orange', 'mango', ['tomato', 'pineapple']]
6
```

The array -> ["tomato","pineapple"] -> This is considered as one single element/item
This is because, the append function can only add a single element/item.

Extend function will add the elements one by one
```
fruits.extend(["tomato","pineapple"])  
print(fruits)  
print(len(fruits))

Output Response -
['apple', 'banana', 'cherry', 'orange', 'mango', ['tomato', 'pineapple'], 'tomato', 'pineapple']
8
```

---
---

2. Remove Function
	1.  If we want to delete/remove one element from the list, we can use the remove function.

```
# Remove Function  
print(f"Remove Function")  

fruitsAgain = ["Apple", "Mango", "Orange"]  
print(f"List of fruits before the remove function is : {fruitsAgain} and the length is {len(fruitsAgain)}")  

fruitsAgain.remove("Orange")  
print(f"List of fruits after the remove function is : {fruitsAgain} and the length is {len(fruitsAgain)}")

Output Response -
Remove Function
List of fruits before the remove function is : ['Apple', 'Mango', 'Orange'] and the length is 3
List of fruits after the remove function is : ['Apple', 'Mango'] and the length is 2
```

---
Now, what happens if we try to delete the element value which is not existing in the list?
```
fruitsAgain.remove("Pineapple")  
print(f"List of fruits after the remove function is : {fruitsAgain} and the length is {len(fruitsAgain)}")

Output Response - 
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Lists in Python\ListOperations-In-Python-2.py", line 36, in <module>
    fruitsAgain.remove("Pineapple")
    ~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^
ValueError: list.remove(x): x not in list
```

Also its case sensitive, assume we have a value named "Orange" in the list, but removing we have just provided "orange", so this also throws similar error.
- It actually looks for the entirely new element/item name "orange"
- When it doesn't find that in the list, it throws an error saying the element is not in list.

---

Question
- Assume we have repetitive values in multiple indexes, so what happens if we perform the remove once?
	- Will the 1st instance gets removed?
	- Will the last instance gets removed?
	- Will both of them gets removed?
Answer
- If there are multiple elements, same value as element in the list and we try to remove it or delete it from the list using the remove function -> The 1st occurrence, 1st position value will be deleted.
- In our example index no 1 and index no 3 had values "Mango" in it, the 1st occurring value i.e that index no 1 gets deleted
```
fruitsAgainAndAgain = ["Apple", "Mango", "Orange", "Mango"]  
print(f"List of fruits before the remove function is : {fruitsAgainAndAgain} and the length is {len(fruitsAgainAndAgain)}")  
  
fruitsAgainAndAgain.remove("Mango")  
print(f"List of fruits after the remove function is : {fruitsAgainAndAgain} and the length is {len(fruitsAgainAndAgain)}")

Output Resposne -
List of fruits before the remove function is : ['Apple', 'Mango', 'Orange', 'Mango'] and the length is 4
List of fruits after the remove function is : ['Apple', 'Orange', 'Mango'] and the length is 3
```

The remove function removes the 1st occurrence of the element present in the list
If the element is not present in the list, we will get an error.

----
---

3. Pop Function
	1. Pop function is also used to delete elements from the list.
	2. Remove function takes an element and deletes that element from the list [the 1st occurrence of it]
	3. Pop function doesn't take the element that needs to be deleted, rather it takes the index at which the value needs to be deleted 
	4. Pop function will remove the value at a particular index

```
# Pop Function  
print("\nPop Function")  

fruitsPop = ["apple", "banana", "cherry"]  
print(fruitsPop)  
fruitsPop.pop(2)  
print(fruitsPop)

Output Response - 
Pop Function
['apple', 'banana', 'cherry']
['apple', 'banana']
```

Can we perfom with the negative index?
- exampe - fruitsPop([-1])
```
fruitsPop2 = ["apple", "banana", "cherry", "mango"]  
print(fruitsPop2)  
fruitsPop2.pop(-1)  
print(fruitsPop2)

Output Response - 
['apple', 'banana', 'cherry', 'mango']
['apple', 'banana', 'cherry']
```

There is another way we can use pop function.
If we want to remove/delete the last element, we can just remove it using just the pop function [without providing any index]

```
fruitsPop3 = ["apple", "banana", "cherry"]  
print(fruitsPop3)  
fruitsPop3.pop()  
print(fruitsPop3)

Output Response -
['apple', 'banana', 'cherry']
['apple', 'banana']
```

----
---


