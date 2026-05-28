
- In previous section, we looked at what is for loop and how for loop works with lists.
- In this section, we shall look how for loop works with other data-types.
	- Strings
	- Tuples
	- Dictionaries

Strings
```
s1 = "Hello World"  
print(s1, type(s1))  
for char in s1:  
    print(char)  
print("End of the loop")

Output Response -
Hello World <class 'str'>
H
e
l
l
o
 
W
o
r
l
d
End of the loop
```

---

Tuples
```
t1 = (1,2,4,10,20,30)  
print(t1, type(t1))  
for num in t1:  
    print(num)  
print("End of the loop")

Output Response -
(1, 2, 4, 10, 20, 30) <class 'tuple'>
1
2
4
10
20
30
End of the loop
```

---

Dictionaries

```
employee = { "emp-id" : 1001, "emp-name" : "Shree", "emp-email" : "shree@shrn.in", "emp-department" : "HR" }  
print(employee, type(employee))  

# to get only the keys  
print("To get only the keys")  
for i in employee:  
    print(i, type(i))
      
# to get only the values  
print("To get only the values")  
for i in employee:  
    print(employee[i])
      
# to get keys and values  
print("To get keys and values")  
for i in employee:  
    print(i, employee[i])
    
Output Response -
{'emp-id': 1001, 'emp-name': 'Shree', 'emp-email': 'shree@shrn.in', 'emp-department': 'HR'} <class 'dict'>

To get only the keys
emp-id <class 'str'>
emp-name <class 'str'>
emp-email <class 'str'>
emp-department <class 'str'>

To get only the values
1001
Shree
shree@shrn.in
HR

To get keys and values
emp-id 1001
emp-name Shree
emp-email shree@shrn.in
emp-department HR
```

---

There is a function called items() in dictionary. It returns the list of items in the key value pairs in the form of a tuple.
Further we can run the for loop on employee.items()

```
# dictionaries items  
print(employee.items(), type(employee))  
for i in employee.items():  
    print(i, type(i))  
    print(i[0],i[1])
    
dict_items([('emp-id', 1001), ('emp-name', 'Shree'), ('emp-email', 'shree@shrn.in'), ('emp-department', 'HR')]) <class 'dict'>
('emp-id', 1001) <class 'tuple'>
emp-id 1001
('emp-name', 'Shree') <class 'tuple'>
emp-name Shree
('emp-email', 'shree@shrn.in') <class 'tuple'>
emp-email shree@shrn.in
('emp-department', 'HR') <class 'tuple'>
emp-department HR
```

---
---



