
1. Reverse Function
	1. Reverse function as the name suggest, it reverses the function.
	2. It changes the list itself [will not create a new list] [changes the existing list]
	3. The 1st element becomes the last element and the last element will become the 1st element and its the same for all other elements as well.
	4. The elements/items of the list gets reversed and its a permanent change in the list.

```
# reverse function [reverse()]  
print("\nReverse Function")  

days_Of_week = ["Mon", "Tue", "Wed", "Thur", "Fri", "Sat", "Sun"]  
print("days_Of_week - before reverse", days_Of_week)  
days_Of_week.reverse()  
print("days_Of_week - after reverse", days_Of_week)

Output Response - 
Reverse Function
days_Of_week - before reverse ['Mon', 'Tue', 'Wed', 'Thur', 'Fri', 'Sat', 'Sun']
days_Of_week - after reverse ['Sun', 'Sat', 'Fri', 'Thur', 'Wed', 'Tue', 'Mon']
```


----
---

2. Sort Function
	1. As the name suggest, the sort function will sort the list into some order.
	2. Important Note - By default it sorts the list into ascending order
		1. Ascending Order - From lesser number to the increasing number order
			1. Basically Ascending order is in Increasing order
	3. If we want to do the sorting in descending order or decreasing order we can use the built-in parameter nums.sort(reverse=True)
		1. If we make reverse=True and if we run the program, our sorted list will be in the descending order or in the reverse order
	4. Also the descending order can be performed by just doing nums.reverse() after it it sorted with ascending order

```
# sort function [sort()]  
print("\nSort Function")  
nums = [4,9,0, 1,2, 8]  
print("nums - before sort", nums)  
nums.sort()  
print("nums - after sort - ascending", nums)  
# nums.reverse()  
# print("nums - after reverse", nums)  
nums.sort(reverse=True)  
print("nums - after sort - reverse/descending", nums)

Output Function - 
Sort Function
nums - before sort [4, 9, 0, 1, 2, 8]
nums - after sort - ascending [0, 1, 2, 4, 8, 9]
nums - after sort - reverse/descending [9, 8, 4, 2, 1, 0]
```

---
---

3. Count Function
	1. Count function as the name suggests and we have seen it in strings, it counts a particular element in the list on how many times it has occurred.
		1. It actually counts how many times the element/item has occurred in the list.
	2. It can be dynamically done through the input function as well.

Positive Approach
```
# count function [count()]  
print("\nCount Function")  
numbers = [ 0, 1, 3, 4 , 1, 0, 5, 0, 0, 3, 0]  
print(f"The list is : {numbers}")  
item_to_count = int(input("Enter the number to be counted from the above list: "))  
count = numbers.count(item_to_count)  
print(f"The Occurrence of {item_to_count} is {count} times")

Output Response -
Count Function
The list is : [0, 1, 3, 4, 1, 0, 5, 0, 0, 3, 0]
Enter the number to be counted from the above list: 0
The Occurrence of 0 is 5 times
```

Negative Approach [ Trying to count the item which is not in the list ]
- It doesn't give an error
	- Count function just counts the number of times a particular element is present in the list.
```
# count function [count()]  
print("\nCount Function")  
numbers = [ 0, 1, 3, 4 , 1, 0, 5, 0, 0, 3, 0]  
print(f"The list is : {numbers}")  
item_to_count = int(input("Enter the number to be counted from the above list: "))  
count = numbers.count(item_to_count)  
print(f"The Occurrence of {item_to_count} is {count} times")

Output Response - 
Count Function
The list is : [0, 1, 3, 4, 1, 0, 5, 0, 0, 3, 0]
Enter the number to be counted from the above list: 7
The Occurrence of 7 is 0 times
```

---

Not necessary integer values only work here, string can also be used.

```
language = ["Python", "Java", "C++", "Python"]  
print(f"\nThe list is : {language}")  
item_to_count_langugage = input("Enter the language to be counted from the above list: ")  
count_language = language.count(item_to_count_langugage)  
print(f"The Occurrence of {item_to_count_langugage} is {count} times")

Output Response - 
The list is : ['Python', 'Java', 'C++', 'Python']
Enter the language to be counted from the above list: Python
The Occurrence of Python is 2 times
```

The value should be provided exactly as declared in the list, if we miss out the case, then the response would be different.
- For example - we have "Python" with capital P in the list, but while the user input if we provide "python" , then the count will not be matched and the response will be 0 times

```
language = ["Python", "Java", "C++", "Python"]  
print(f"\nThe list is : {language}")  
item_to_count_langugage = input("Enter the language to be counted from the above list: ")  
count_language = language.count(item_to_count_langugage)  
print(f"The Occurrence of {item_to_count_langugage} is {count} times")

Output Response - 
The list is : ['Python', 'Java', 'C++', 'Python']
Enter the language to be counted from the above list: python
The Occurrence of python is 0 times
```

----
---

4. Membership Operator
	1. The membership operator is represented as [in]
	2. "in" checks if a particular element/item present in the list or not.
	3. We can use count function to also check it
		1. If the count is 0, it means the element is not present
		2. If the count is positive, it means the element is present
	4. "in" will gives us True - If the item is present
	5. "in" will gives us False - If the item is not present

```
# membership operation [ in ]  
language_in = ["Python", "Java", "C++", "Python"]  
print(f"\nThe list is : {language_in}")
print("'in operation'")  
print("Python" in language_in)  
print("Java" in language_in)  
print("Javascript" in language_in)

Output Response - 
The list is : ['Python', 'Java', 'C++', 'Python']
'in operation'
True
True
False
```

Similarly we have "not in" operator - Its basically a reverse of "in"
- "not in" => returns true when element is not present in the list
- "not in"  => returns false when element is present in the list

```
language_in = ["Python", "Java", "C++", "Python"]  
print(f"\nThe list is : {language_in}")

print("'not in' operation")  
print("C++" not in language_in)  
print("JavaScript" not in language_in)

Output Response - 
'not in' operation
False
True
```


---
---
