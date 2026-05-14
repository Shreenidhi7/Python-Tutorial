
In previous section, we looked at the tuples and how they are different from lists, when to use tuples, indexing of tuples and how to create tuples in mutiple ways

In this section, we shall look at basic operations on tuples
1. Concatenation
2. Repetition
3. Membership
4. Count
5. Index
6. Min
7. Max
8. Sum

---

1. Concatenation
	1. We have 2 tuple in which we have stored the values
		1. student_details1 = (1001, "Shree")  
		2. student_details2 = (78.5, 91.0, 83.5, 79.5)
	2. If we want to combine these 2 information into a single tuple
		1. We can use the concatenation operator ( + operator )
			1. It joins the 2 tuples together

```
# concatenation [+]
print(f"tuple - concatenation operation")  
student_details1 = (1001, "Shree")  
student_details2 = (78.5, 91.0, 83.5, 79.5)  
student_details3 = student_details1 + student_details2  
print(f'concatenation of 2 tuple into 1 : {student_details3}')

Output Response -
tuple - concatenation operation
concatenation of 2 tuple into 1 : (1001, 'Shree', 78.5, 91.0, 83.5, 79.5)
```

----

2. Repetition ( * operator)
	1. Its used to if we want to repeat something in case of list/string/tuple
	2. If we want to replicate the information multiple times, we can use the repetition operator

```
# repetition [*]
print(f'tuple - repetition operation')  
t1 = ("Class 5", 5000)  
print(f"repetition of tuple : {t1*3}")

Output Response - 
tuple - repetition operation
repetition of tuple : ('Class 5', 5000, 'Class 5', 5000, 'Class 5', 5000)
```

---

3. Membership [in, not in]
	1. In -> It checks if a particular element is part of the list/string/tuple
	2. Not In -> It checks if a particular element is not part of the list/string/tuple

```
# membership [in,not in]  
print(f'tuple - membership operation')  
print("student details", student_details3)  
  
print(f" -in-membership")  
print(f" is a member: {91.0 in student_details3}")  
print(f" is a member: {84.5 in student_details3}")  
  
print(f" -not-in-membership")  
print(f" is a member: {92.0 not in student_details3}")  
print(f" is a member: {78.5 not in student_details3}")

Output Response -
student details (1001, 'Shree', 78.5, 91.0, 83.5, 79.5)
 -in-membership
 is a member: True
 is a member: False
 -not-in-membership
 is a member: True
 is a member: False
```

---

We discussed that the major difference b/w list and tuple is we cannot do modification operations on a tuple
When a tuple is created, it can be re-assigned to some other tuple or any other data, but we cannot add to an existing tuple
Adding/Removing (Any Modifications ) on the tuple - Its not possible
But we can do some read operations on tuple - example - count

4. Count