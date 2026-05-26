
- In previous section we discussed about creating dictionaries, key-values pairs in dictionaries and how to update a dictionary by changing a value or adding a new key value pair to a dictionary
- In this section, we shall discuss more operations with dictionaries

1. Fetching the value from the dictionary
	1. Basically, we use the key to get the value of the key.
	2. But there is a function called get() in dictionary which does the similar task
	3. There is a difference between the usual key fetch and the get() function.
		1. If we try to retrieve/fetch the value from the key which doen't exist, we get an Error - Key Error
		2. But if we try to retrieve/fetch the value form the get() method, then we won't get the error, but we get "None" as the output.
		3. Observation - When we use square bracket to fetch the value which is not present, we get an error.  But if we use a get() function, we don't get an error first of all, but we get the output as None
			1. Why None?
					1. Its because there is no key in the dictionary
		4. If we are not sure about the element is present in the dictionary, to avoid the error we get use get() function where it returns "None" as the output instead of throwing an Error

Using Square Brackets []
```
student1 = {"maths" : " 80.5", "english" : " 97.5", "physics" : " 97.5"}  
  
# fetch the key's value using square brackets  
print(f"positive case - using [] brackets : {student1["english"]}")  
# print(f"negative case - using [] brackets : {student1["french"]}")

Output Response -
positive case - using [] brackets :  97.5
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\OperationsOnDictionaries.py", line 5, in <module>
    print(f"negative case - using [] brackets : {student1["french"]}")
                                                 ~~~~~~~~^^^^^^^^^^
KeyError: 'french'
```

Using Get() Function
```
student1 = {"maths" : " 80.5", "english" : " 97.5", "physics" : " 97.5"}  
  
# fetch the key's value using the get() function  
print(f"positive case - using get() function : {student1.get('english')}")  
print(f"negative case - using get() function : {student1.get('kannada')}")

Output Response -
positive case - using get() function :  97.5
negative case - using get() function : None
```

---

- There is another option with Get()
	- Lets say if the key is not present, i want some default value to be used for that specific key instead of None
	- Lets say the students chemistry marks is not present, but i want the marks to be printed as 40
		- When i run this, i get 40.0 instead of None

```
emp1 = {"id" : 1001, "name" : "John", "salary" : 10000}  
print(emp1.get("phone",9876543210))

Output Response -
9876543210
```

- If we have the values assigned for the key, and while fetching even though we provide the DEFAULT value, the initially assigned value will only be returned.
```
emp1 = {"id" : 1001, "name" : "John", "salary" : 10000}  
print(emp1.get("phone",9876543210))  
print(emp1.get("id",111111111111))

Output Response - 
9876543210
1001
```

----
---

2. Membership Operator
	1. To verify if a particular element or item is present in the list/tuple/string we use membership operator.
	2. In dictionaries, membership operator doesn't look for the value, but it looks for the key.
		1. If the key is present, it gives us True
		2. If the key is not present, it gives us False

```
print(f"Membership Operators in Dictionaries")  
print("id" in emp1)  
print("name" in emp1)  
print(1001 in emp1)  
print("John" in emp1)

Output Response -
True
True
False
False
```

---
---

3. Updating the Dictionary
	1. Update function basically updates the key value pairs of another dictionary inside the existing dictionary
```
print(f"Updating the Dictionary")  
sem1_marks = {"marks" : 78.5, "english" : 71.0, "physics" : 86.5}  
sem2_marks = {"chemistry": 81.5, "biology": 90.5}  
sem1_marks.update(sem2_marks)  
print(sem1_marks)

Output Response -
Updating the Dictionary
{'marks': 78.5, 'english': 71.0, 'physics': 86.5, 'chemistry': 81.5, 'biology': 90.5}
```

- Assume we have 2 dictionaries
	- groceries_1 is my main dictionary and groceries_2 is the updated/new items that we have got
	- groceries_1 is my dictionary with the stock that i have and groceries_2 is the new stock that i have.
		- groceries_1 = {"milk" : 60, "rice" : 100, "biscuits" : 200}  
		- groceries_2 = {"rice" : 110, "bread" : 30}
	- Here there are  2 things, we have rice in groceries_2 which i already have it in my groceries_1 with price of 100, but i have got a new stock with the updated price of 110 and also i have got a new item bread with price of 30
	- Now, if i do groceries_1.update(groceries_2)
		- Since we have the rice already in groceries_1, the price of rice will get updated and since bread is not present in groceries_1, the bread value gets added [a ney key-value pair will be added]
		- {'milk': 60, 'rice': 110, 'biscuits': 200, 'bread': 30}
		- The price of rice gets updated and new item bread gets added to the dictionary
		- This is update function
```
print(f"Updating the Dictionary")  
sem1_marks = {"marks" : 78.5, "english" : 71.0, "physics" : 86.5}  
sem2_marks = {"chemistry": 81.5, "biology": 90.5}  
sem1_marks.update(sem2_marks)  
print(sem1_marks)  
  
groceries_1 = {"milk" : 60, "rice" : 100, "biscuits" : 200}  
groceries_2 = {"rice" : 110, "bread" : 30}  
groceries_1.update(groceries_2)  
print(groceries_1)

Output Response -
Updating the Dictionary
{'marks': 78.5, 'english': 71.0, 'physics': 86.5, 'chemistry': 81.5, 'biology': 90.5}
{'milk': 60, 'rice': 110, 'biscuits': 200, 'bread': 30}
```

---
---

4. Deleting the item from the Dictionary
	1. We can use Pop() function to delete/remove an item [key-value pair] from the dictionary

```
print(f"Deleting an item from the Dictionary")  
groceries_3 = {'milk': 60, 'rice': 110, 'biscuits': 200, 'bread': 30}  
print(groceries_3)  
groceries_3.pop('milk')  
print(groceries_3)

Output Response -
Deleting an item from the Dictionary
{'milk': 60, 'rice': 110, 'biscuits': 200, 'bread': 30}
{'rice': 110, 'biscuits': 200, 'bread': 30}
```

---
---

5. Keys cannot be Duplicated
	1. Even though while creating a dictionary, if we create a duplicate key with different value, there wont be any error, but the last instance of the key which is declared, that will only be considered.
		1. This is because, when python reads the dictionary, it reads from left to right
		2. So the key which is used twice while creating and one thing to note here is Keys cannot be duplicated in the dictonary
			1. Keys should be unique
		3. The value of the duplicated key will be value which is most recent/latest value
			1. From Left to Right - Whichever value is at the right, that value will be considered

```
print("Keys duplication Test")  
groceries_4 = {'milk': 60, 'rice': 110, 'bread': 30, "milk" : 100}  
print(groceries_4)

Output Response - 
Keys duplication Test
{'milk': 100, 'rice': 110, 'bread': 30}
```

---
---

