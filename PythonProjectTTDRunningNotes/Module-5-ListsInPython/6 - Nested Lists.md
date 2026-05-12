
In this section, we shall look at Nested Lists
Nested lists are nothing but a list inside another list.
Until now what we have seen is that a list can have any element or data type as an element of the list. 
It can have an integer, float, string, Boolean, none and a list itself can be an item or an element of a list.
Example - 
- l1 = [5, 1.5, "Python", True, None, [1,2,3], 10]
- print(len(l1))
	- 7
- print(l1[-2])
	- [1,2,3]
- [1,2,3] in l1 is called nested list.

- Question
	- Can we fetch the elements/items from the internal list
		- if we call [1,2,3] as the internal list, can we fetch for example 1 from the internal/nested list?
- Answer
	- Yes, 1st we need to fetch the inner list [the list itself]
	- 1st fetch the [-2] element of the outer list l1 -> this will fetch us the entire list [1,2,3] and then of that list, if we need to fetch the 1st element, we shall do [0] (that would be element number 1)
	- print(l1[-2][0])

```
# List inside a list  
l1 = [5, 1.5, "Python", True, None, [1,2,3], 10]  
print(l1)  
print(len(l1))  
# printing 2nd last element  
print(l1[-2])  
# can we fetch the element/item from the internal list  
print(l1[-2][0])

Output Response -
[5, 1.5, 'Python', True, None, [1, 2, 3], 10]
7
[1, 2, 3]
1
```


Also, there is no such restrictions of creating a list inside a list.
Example -
- l2 = [[1,2],[3,4],[5,6,[0,7]]]
- print(len(l2))
	- 3
Lets say, we have to fetch 7, how do we fetch it?
- 1st we have to fetch the element - [5,6, [0,7]]
- Then we have to fetch the element from [0,7]

```
l2 = [[1,2],[3,4],[5,6,[0,7]]]  
print(l2)  
print(len(l2))
l2a = l2[-1]  
print(l2a)  
l2a1 = l2a[-1]  
print(l2a1)  
l2a2 = l2a1[-1]  
print(l2a2)

# direct way to fetch  
print(l2[-1][-1][-1])

Output Response - 
[[1, 2], [3, 4], [5, 6, [0, 7]]]
3
[5, 6, [0, 7]]
[0, 7]
7

7
```


----
---
