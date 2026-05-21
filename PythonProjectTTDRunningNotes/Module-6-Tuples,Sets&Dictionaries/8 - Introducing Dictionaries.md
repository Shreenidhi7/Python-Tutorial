
- In this section, we shall get introduced to a new data-type in python called Dictionaries.
- A English-to-English Dictionary have some words and along with that it has its meaning.
- There are 2 entities, the word and the meaning of it.
- Its similar to Sets, But sets have single element enclosed within curly brackets in a comma separated way
- In Python as well, Dictionaries have something called **a key and value pair**
	- Also they are comma separated key-value pairs enclosed within curly brackets
	- Each Key-Value pair is separated by colons.
	- Example - 
		- {key1:value1, key2:value2, ...}
- Why do we use Dictionaries?
	- Example => Groceries Bill
		- The name of the grocery and the price of the grocery
```
# comma separated key value pairs enclosed within curly brackets  
# syntax = {key1:value1, key2: value2, ...}  
  
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))

Output Response -
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
```

- milk is the key, 60 is the value
- biscuits is the key, 20 is the value
- rice is the key, 90 is the value
- bread is the key, 30 is the value

---

**Length**
- We can use the len function in dictionaries as well.
- We have seen earlier that len function is used to find out a total number of elements in a data-type
	- Tuples, Lists, Strings, Sets
- Here in Dictionaries, we do not have elements, but a pairs [key and value pairs]
	- Each of them are called Pairs
- So, if we use len function with groceries example, we will get how many key value pairs are present in the dictionary
```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))  
print(len(groceries))

Output Response - 
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
4
```

---

**Indexing**
- Do we have indexing in Dictionaries?
	- No, we don't have

```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))  
print(groceries[0])

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\8-IntroductionToDictionaries.py", line 7, in <module>
    print(groceries[0])
          ~~~~~~~~~^^^
KeyError: 0
```

---

Question
- If we don't have indexing, then how can we fetch the values from the Dictionaries?
Answer
- To fetch the **"VALUE"** from the dictionary, we have use the **"KEY"**
- We don't have indexing in Dictionary, but the values can be fetched using the key
- So, if i want to know the price of the milk in the below example
	- print(groceries["milk"])

```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))  
# print(len(groceries))  
print(groceries["milk"])

Output Response -
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
60
```

- To fetch the value from the dictionary, we need to use the key, we cannot use indexing in dictionary
- Dictionaries can be created in multiple way

---

Question
- Can we modify a dictionary's value? Also logically should dictionary should be allowed to change a value?
Answer
- This goes to the concept of mutability.
- If Dictionaries are mutable, we should be able to change the value
- Yes, dictionary should be allowed to change a value.
- Below is the example on how to change a value using the assignment operator.

```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries)) 
groceries["milk"] = 65  
print(groceries, type(groceries))

Output Response - 
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
{'milk': 65, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
```

---

Question
- What happens when we try to print or change the value of the key that doesn't exist?
	- Trying to fetch somethings which doesn't exist.
Answer
- We should get an error and it should be KeyError.
	- It means the key is not present in the dictionary
		- If the Key is not present, we cannot fetch the value obviously and we will get an error as well.

```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))
print(groceries["eggs"])

Output Response - 
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\8-IntroductionToDictionaries.py", line 11, in <module>
    print(groceries["eggs"])
          ~~~~~~~~~^^^^^^^^
KeyError: 'eggs'

```

---

Question
- Can we try to change the value of key which doesn't exist at all?
	- Assume the key doesn't exist in dictionary
Answer
- It gets executed and there are no errors and we can see that the key which we try to change the value gets added to the dictionary
- The syntax of changing the value of the key holds good for added a new key to the dictionary as well
- It adds new key-value pair to the dictionary
- If we do the same syntax of the key which is already existing in the list, here the value gets updated. 
- [If the key is present, the value of the key gets updated in the dictionary]
- [If the key is not present, the key-value pair is added to the dictionary]

```
groceries = {"milk":60, "biscuits":20, "rice": 90, "bread": 30}  
print(groceries, type(groceries))  

groceries["eggs"] = 10 # adds new key-value pair to the dictionary  
print(groceries, type(groceries))  

groceries["bread"] = 50 # updates the value of the key  
print(groceries, type(groceries))

Output Response -
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30} <class 'dict'>
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 30, 'eggs': 10} <class 'dict'>
{'milk': 60, 'biscuits': 20, 'rice': 90, 'bread': 50, 'eggs': 10} <class 'dict'>
```

---
---
