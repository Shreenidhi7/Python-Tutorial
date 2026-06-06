
- In previous section, we looked at what is lamba function and how to create lambda functions.
- This section, we will look at 2 functions - filter() and map() functions that basically utilize lambda functions.

1. Filter()
	1. The filter function in Python takes function as the argument and a sequence as the second argument.
		1. 1st argument - function
		2. 2nd argument - sequence[List/Tuple/Etc]
	2. This offers an elegant way of filtering all the elements for particular sequence for which the function returns True
	3. Example - For each element of "seq", the filter function will call the lambda function "odd"
		1. When the output is True, we get that element in the filter object
			1. 1 % 2 != 0 => True
				1. It is True, so value 1 will be kept in filter object
			2. 2 % 2 != 0 => False
				1. It is False, so the value 2 will be discarded.
			3. 3 % 2 !=0 => True
				1. It is True, so the value 3 will be kept in the filter object
			4. 4 % 2 !=0 => False
				1. It is False, so the value 4 will be discarded.
		2. The filtered objects are kept in the form of object.
		3. In order to visually see the filtered elements, we can typecast the output to list, so the filtered values are displayed
	4. To understand, Filter() function will keep the values of a particular sequence/list/tuple for which the function gives True
	5. And for the values of the sequence or the list for which the function gives False, those values will be filtered out (they will be discarded)
		1. Thats the reason, its called Filter fucntion.

```
# filter(function, sequence)  
  
seq = [1,2,3,4]  
odd = lambda x : True if x % 2 !=0 else False  
filtered_output = filter(odd, seq)  
print(f"Filtered Object Output - {filtered_output}")  
print(f"Odd numbers in the above sequence - {list(filtered_output)}")

Output Response -
Filtered Object Output - <filter object at 0x0000021E60C06DA0>
Odd numbers in the above sequence - [1, 3]
```

- Simplified Form
	- We can directly pass the function inside the filter function
```
seq = [1,2,3,4]  
filtered_output = filter(lambda x : True if x % 2 !=0 else False, seq)  
print(f"Filtered Object Output - {filtered_output}")  
print(f"Odd numbers in the above sequence - {list(filtered_output)}")

Output Response -
Filtered Object Output - <filter object at 0x0000021E60C06DA0>
Odd numbers in the above sequence - [1, 3]
```

---
---

2. Map()
	1. Map function also takes a function as the 1st arguments an sequence as the 2nd argument
		1. 1st argument - function
		2. 2nd argument - sequence[List/Tuple/Etc]
	2. If we run the above similar function with the map function
		1. Map function will not do any filtering, but whatever the ouput for each element of the sequence will be kept in map function.
		2. . 1 % 2 != 0 => True
				1. It is True, so a map object is created as True
			1. 2 % 2 != 0 => False
				1. It is False, so a map object is created as False
			2. 3 % 2 !=0 => True
				1. It is True, so a map object is created as True
			3. 4 % 2 !=0 => False
				1. It is False, so a map object is created as False
		3. Main Difference between Filter and Map function is that
			1. Filter function will keep the element/value of the sequence for which we get a True
			2. Map function will keep the value as True/False for all the sequence based on the condition check
```
# map(function,sequence)  
seq = [1,2,3,4]  
mapped_output = map(lambda x : True if x % 2 !=0 else False, seq)  
print(f"Mapped Object Output - {mapped_output}")  
print(f"Odd numbers in the above sequence - {list(mapped_output)}")

Output Response -
Mapped Object Output - <map object at 0x000001D8179B1E40>
Odd numbers in the above sequence - [True, False, True, False]
```

- In these odd/even scenarios, Filter will be better in these case
- Map will be useful wherein we have a sequence in which we want to do certain operations on each element of the sequence
	- Example - We simply want to square all the elements

```
seq = [1,2,3,4]  
mapped_output = map(lambda x :  x ** 2, seq)  
print(f"Mapped Object Output - {mapped_output}")  
print(f"Square of the elements in the above sequence - {list(mapped_output)}")

Output Response -
Mapped Object Output - <map object at 0x0000013894A42780>
Square of the elements in the above sequence - [1, 4, 9, 16]
```

- So, map iterates through all the elements in the sequence and applies the logic on that and all the output will be stored in the map object  and then we can convert it into a list/tuple depending on what we want.


---
---
