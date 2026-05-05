
In this section we shall continue on list, but we will look at certain operations on list.

1. Slicing of List
	1. Slicing of Lists is similar to Slicing in Strings
		1. When we do a slicing on a list, we get list in return
	2. Syntax = list[start:end:step]
		1. start index - it will be included
		2. end index - it will not be included
		3. step index - it like how many step to take at a time
	3. Example - 
		1. l1 = [3,8,1,0,4,9,7,3,6]  
		2. print(l1[1:6:1])
		3. Output - [8, 1, 0, 4, 9]
```
# Slicing of Lists in Python  
  
l1 = [3,8,1,0,4,9,7,3,6]  
print(len(l1))  
print(l1[1:6:1])
print(l1[2:7:2])

Output Response - 
9
[8, 1, 0, 4, 9]
[1, 4, 7]
```

---
---

2. Concatenation of Lists
	1. Its similar to concatenation of strings
		1. It called joining of lists together.
	2. Concatenation can be done with the Plus [ +] operator
	3. Example =
		1. l1 = [1, 7, 2]
		2. l2 = [0, 5]
		3. print(l1 + l2)
			1. Output - [1, 7, 2, 0, 5]
		4. We can see that the elements of l1 is printed 1st and then the elements of the l2
		5. If we want to print the reverse of the above, it can be done
			1. print(l2 + l1)
				1. Output - [0 , 5, 1, 7, 2]

```
# Concatenation of Lists in Python  
print("\nConcatenation of Lists")  
  
l2 = [ 1, 7, 2]  
l3 = [0, 5]  
print(l2 + l3)  
print(l3 + l2)

Output Response - 
Concatenation of Lists
[1, 7, 2, 0, 5]
[0, 5, 1, 7, 2]
```

----
----

3. Repetition of Lists
	1. Repetition operator is the Star Operator ( * ) 
	2. It is similar to the repetition in strings
	3. Example -
		1. l3 = [0, 5]
		2. print(l3 * 3)
			1. Output -
				1. [0, 5, 0, 5, 0, 5]
		3. Here l3 * 3 => It will repeat the elements of l3 list 3 times.
		4. They are repeated inside a single list
		5. The elements are repeated and stored in a same list in the output.

```
# Repetition of Lists in Python  
l3 = [0, 5]
print("\nRepetition of Lists")  
print(l3 * 3)

Output Response - 
Repetition of Lists
[0, 5, 0, 5, 0, 5]
```

---
---

Now, we shall discuss some functions/methods that we can use with lists
The 1st function that we have is APPEND function [append()]

4. Append()
	1. This function basically adds an item to the end of the list.
	2. One item is added at the end of the list.
	3. The item could be of any data type.
	4. Example - 
		1. fruits = ["Mango", "Apple", "Orange"]
		2. print(fruits)
	5. Now, append function can be applied on the list.
		1. Syntax - list.append(item)
				1. fruits.append("Banana")
				2. print(fruits)
	6. Important Thing to Note -
		1. We cannot directly print => print(fruits.append("Banana"))
		2. If we print => we get the output as None => It represents No Value
		3. In String, if we print similar to this, we get an output
			1. s1 = "Python is fun"
			2. print(s1.replace("Python", "Java"))
			3. Output => Java is fun
		4. But the same thing doesn't happen with List
			1. Because there is a very basic difference b/w String and Lists
			2. When we perform any operation on a String, the whole string is refactored/changed to the new change.
			3. But its not the same in Lists
					1. Functions in Lists doesn't return the updated list.
					2. The List gets updated
					3. It doesn't create a new list as compared to the Strings
						1. When we do s1.replace(old, new) => we get a new string.
			4. In Lists, If we use any function
				1. In Append -> It actually acts "Banana" to the existing list
				2. The existing list itself will get changed
					1. This is called MUTABILITY
	7. So, append() function adds "Banana" to the existing list and the existing list gets updated/changed
		1. Lists when used with any function, the existing list only gets changed
	8. Append Function Always add an element at the end of the list.
			1. We cannot add it in the middle or at the front.
```
# Functions in List  
# Append Function  
print("\nAppend Function")  

fruits = ["mango", "apple", "orange"]  
print(fruits)  
fruits.append("banana")  
print(fruits)

Output Response - 
Append Function
['mango', 'apple', 'orange']
['mango', 'apple', 'orange', 'banana']
```

---
---

5. Insert Function
	1. If we want to specify where an item needs to be added [be it at the front or at the middle], we use the function called Insert
		1. Adds an element before the specified index
		2. Syntax = list.insert(index, item)

```
# insert function  
## adds an element before the specified index  
# syntax = list.insert(index,item)  

print("\nInsert Function")  
print(f"Before Inserting Function {fruits}")  
fruits.insert(2, "cherry")  
print(f"After Inserting Function {fruits}")

Output Response - 
Insert Function
Before Inserting Function ['mango', 'apple', 'orange', 'banana']
After Inserting Function ['mango', 'apple', 'cherry', 'orange', 'banana']
```

----
---
