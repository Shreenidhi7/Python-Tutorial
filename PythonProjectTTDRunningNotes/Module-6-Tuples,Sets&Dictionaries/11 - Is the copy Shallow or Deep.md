
1. Shallow Copy/Deep Copy concepts are applied for mutable data types
	1. Mutable data types - List, Set, Dictionary - The data types on which the state can be changed.

2. Copy Function
	1. Lets consider a list
		1. l1 = l1 = [1, 2.5, [10,20,30], "Python"]
	2. If we want to copy this list, there are certain ways to do it.
		1. Copy Function
		2. Using a Copy Function of the module called Copy
			1. In Keyword section, we had imported a module called keyword to list down all the keyword present in the Python that we have installed.
			2. Similarly there is a module called "copy", but this copy module is an internal module to Python which has a couple of functions
				1. Copy
				2. Deep Copy
			3. Copy function of the copy module is used to create shallow copy as well.

- Lets use this copy module to basically copy the lists both shallow and deep.
- For using the copy function and the deep copy function, we have to import the module using import syntax like import copy.
- We will learn about module in details later, but below is how we can use import a module that is present in python.

- When we create a list, this list will have a memory location
	- l1 = [1, 2.5, [10,20,30], "Python"]
- We know that whenever a variable is created with a value, a memory address will be there and in that memory address the values will be stored and the variable will be referring to that memory address.
	- l1 will have some memory address and it will do a copy.copy - which is a shallow copy.
	- l2 will be created in a different memory location or we can say the same value will be stored in a different memory with the same structure list and l2 will refer to that memory location
	- In short, both l1 & l2 have different memory address
	- We can confirm that the memory address of l1 and l2 by printing id(l1) & l2(id)

```
import copy  
  
# list  
l1 = [1, 2.5, [10,20,30], "Python"]  
print("l1 -",l1)  
print("memory address of l1", id(l1))  
l2 = copy.copy(l1)  
print("l2 -",l2)  
print("memory address of l2", id(l2))

Output Response -
l1 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l1 2817697304512
l2 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l2 2817701030016
```


---
---

1. When we have the list l1 = l1 = [1, 2.5, [10,20,30], "Python"] and we have a memory address to it.
2. When we create a copy l2 = copy.copy(l1) => This is a shallow copy
	1. This l2 gets created in a new memory location
3. But the internal values (1, 2.5, [10,20,30], "Python") will also have some memory address of its own
	1. The inner values will also have their own memory addresses
	2. These memory addresses are not copied or they are not different -> They are the same
	3. The memory address of the inner values like (1,2.5, [10,20,30], "Python") are same
	4. l1 list and l2 list have memory address different, but the inner elements don't have memory address different
	5. When we change l1[0] = 5 => this gets re-assigned from value 1 to 5
	6. When we change the 1st element of the inner list to 50 (it was 10 earlier), the memory address of the earlier one is for example 1009, the list l2 will also have the same memory address 1009
		1. Basically inner lists are referring to the same memory location.
		2. So, when we change it to 50, the first l1 will also gets reflected because both the memory address are same.
	7. Why l1[0] doesn't get reflected, its because we are directly changing the value - This is called Replacement.
		1. l1 [2] [0] => This is changing the inner element, so when we change the inner element in the list, the memory address of the inner list doesn't gets changed - it remains the same, we are not re-assigning fully/we are not changing the list fully.
			1. We are just changing the elements of the list.
			2. The list stays there, but only the element changes
			3. Since l1 and l2 have same values, it gets reflected here as well.
		2. **This is the reason its called shallow copy because the outer list only has the different memory address. The inner lists will have the same memory address**

```
# shallow copy  
# list  
l1 = [1, 2.5, [10,20,30], "Python"]  
print("l1 -",l1)  
print("memory address of l1", id(l1))  
l2 = copy.copy(l1)  
print("l2 -",l2)  
print("memory address of l2", id(l2))  
l1[0] = 5  
l1[2][0] = 50  
print(f"l1 -> {l1}", id(l1))  
print(f"l2 -> {l2}", id(l2))

Output Response -
l1 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l1 1582923894720
l2 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l2 1582927620224
l1 -> [5, 2.5, [50, 20, 30], 'Python'] 1582923894720
l2 -> [1, 2.5, [50, 20, 30], 'Python'] 1582927620224
```

---
---

This could be a problem in cases wherein we want to have a value, have a list which is original and you want to change the copied one, not the existing one/not the original one - In that case the shallow copy wont work - Because if we change the l2 it will reflect in l1
- So to avoid this kind of reflection of an inner element change in either of them, there is a concept of deep copy.
- Deep Copy is a concept wherein the inner elements also gets copied at different time.
- Function - copy.deepcopy()
	- When we do a deepcopy, the memory addresses of l1 and l2 are different but memory address.
	- So when we change the inner list from 10 to 50

```
# deep copy  
# list  
l1 = [1, 2.5, [10,20,30], "Python"]  
print("l1 -",l1)  
print("memory address of l1", id(l1))  
l2 = copy.deepcopy(l1)  
print("l2 -",l2)  
print("memory address of l2", id(l2))  
l1[0] = 5  
l1[2][0] = 50  
print(f"l1 -> {l1}", id(l1))  
print(f"l2 -> {l2}", id(l2))

Output Response -
l1 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l1 1650315218880
l2 - [1, 2.5, [10, 20, 30], 'Python']
memory address of l2 1650319075456
l1 -> [5, 2.5, [50, 20, 30], 'Python'] 1650315218880
l2 -> [1, 2.5, [10, 20, 30], 'Python'] 1650319075456
```

---
---

Shallow copy is creating a new list at a different memory location, the inner elements of the list, doesn't get copied
If any changes made to the nested item or the element of the copied list, it gets reflected in the original list

Deep copy, the nested inner elements will also have a different memory location.
It means any changes made here will not get reflected.
This also can be done in mutable objects 

---
---

Dictionary

Shallow Copy
```
# dictionary  
# shallow copy  
d1 = {"id" : 1111, "name" : "John", "marks": {"eng": 71.5, "maths" : 91.5, "bio" : 80.0}}  
print("d1",d1)  
d2 = copy.copy(d1)  
print("d2",d2)  
d1["name"] = "Dan"  
d1["marks"]["maths"] = 92.5  
print(f"d1 {d1}", id(d1))  
print(f"d2 {d2}", id(d2))

Output Response -
d1 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 91.5, 'bio': 80.0}}
d2 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 91.5, 'bio': 80.0}}
d1 {'id': 1111, 'name': 'Dan', 'marks': {'eng': 71.5, 'maths': 92.5, 'bio': 80.0}} 2203263881920
d2 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 92.5, 'bio': 80.0}} 2203265609856
```


Deep Copy
```
# dictionary  
# deep copy  
d1 = {"id" : 1111, "name" : "John", "marks": {"eng": 71.5, "maths" : 91.5, "bio" : 80.0}}  
print("d1",d1)  
d2 = copy.deepcopy(d1)  
print("d2",d2)  
d1["name"] = "Dan"  
d1["marks"]["maths"] = 92.5  
print(f"d1 {d1}", id(d1))  
print(f"d2 {d2}", id(d2))

Output Response -

d1 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 91.5, 'bio': 80.0}}
d2 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 91.5, 'bio': 80.0}}
d1 {'id': 1111, 'name': 'Dan', 'marks': {'eng': 71.5, 'maths': 92.5, 'bio': 80.0}} 2611952603840
d2 {'id': 1111, 'name': 'John', 'marks': {'eng': 71.5, 'maths': 91.5, 'bio': 80.0}} 2611954331904
```


---
---
