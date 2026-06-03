
- In previous section, we looked at "star args" [ * args ] -> which allows us to take variable length positional arguments.
-  N number of arguments can be passed to be received by star args [ * args ]

- In this section, we will look at Variable Length Arguments only but Variable Length Keyword Argument
	- Variable Length Keyword Argument is used to take 0 or more arguments or variable length keyword arguments
	- Its represented by
		- [ ** kw args ] - variable length keyword arguments
			- Its a convention to be followed, not a strict variable that needs to be used.

```
# **kwargs - variable length keyword arguments (o to m)  
  
def func(**kwargs):  
    print(kwargs, type(kwargs))  
  
func(x=10, y=20)

Output Response - 
{'x': 10, 'y': 20} <class 'dict'>
```

- x = 10, y = 20 goes to keyword argument to [ ** kwargs ]
	- [ ** ] means it can 0 or more keyword arguments
	- They are stored in a Dictionary
		- kwargs is a dictionary
	- kwargs is a convention that needs to be followed for writing the keyword argument of variable length but we can use something else as well.
	- Also we can have 0 or more keyword arguments passed.
		- If we don't give any arguments, it will be an empty dictionary

```
# empty dictionary without any arguments passed  
def func(**kwargs):  
    print(kwargs, type(kwargs))  
  
func()

Output Response -
{} <class 'dict'>

```

- Since this is a keyword argument, the default argument should be at the last
	- There shouldn't be ** at the 1st.

```
def student_details(sid, sname, **marks):  
    if len(marks) == 0:  
        print(f"{sname} did not attend the exam")  
    else:  
        present = sum(marks.values()) / len(marks)  
        print(f"{sname} with id {sid} secured {present}%")  
  
student_details(101, "Shree", sub1 = 78.95, sub2 = 81.00, sub3 = 93.72)  
student_details(201, "Nidhi", sub4 = 73.33, sub5 = 86.66, sub6 = 99.99, sub7 = 60.00)

Output Response -
Shree with id 101 secured 84.55666666666667%
Nidhi with id 201 secured 79.995%
```

- Important Note -
	- There can be both keyword argument and positional argument at the same function
	- But positional argument should be 1st and then keyword arguement has to be followed
		- def student_details(sid, sname,* extra , * * marks):  

```
def student_details(sid, sname, *extra, **marks):  
    if len(marks) == 0:  
        print(f"{sname} did not attend the exam")  
    else:  
        present = sum(marks.values()) / len(marks)  
        print(f"{sname} with id {sid} secured {present}%")  
    print(f"{sname} does {extra} time")  
  
student_details(101, "Shree", "Footbal" , sub1 = 78.95, sub2 = 81.00, sub3 = 93.72)  
student_details(201, "Nidhi", "Cricket", "Hockey" ,sub4 = 73.33, sub5 = 86.66, sub6 = 99.99, sub7 = 60.00)

Output Response -
Shree with id 101 secured 84.55666666666667%
Shree does ('Footbal',) time
Nidhi with id 201 secured 79.995%
Nidhi does ('Cricket', 'Hockey') time
```

---
---

