
- In previous section, we looked at positional arguments, default arguments and keyword arguments.
- In this section, we shall look at variable length argument

Question
- What if we need to add a variable length number of values in a function?
	- It means we don't know numbers we are trying to add.
	- Also our function should be created in such a way that it should allow us to take 2,3,4..50 values
	- And it should add all those numbers and give output to us.
Answer
- For all the above requements, we use variable length arguments
	- Its called star args [ * args ] in python
		- [ * args ] means N number of variable length argument.
		- * means it allows the arguments "args" to take 0 or more number of arguments.
		- Even if we give 0 arguments - it will work
		- If we give 2 arguments, it will work 

```
# *args - variable length positional arguments (o to m)  
def add(*args):  
    print(args, type(args))  
  
add(10,20,30,40,50)

Output Response -
(10, 20, 30, 40, 50) <class 'tuple'>
```

- when we pass the number of arguments, number of values to star args -> this gets stored in a variable callled args as a tuple
- Important Note: We shouldn't use * while using the value [while using the tupe, we shouldn't * ]
	- Only while accepting the values, we have to use the function definition with * args

```
def add(*args):  
    print(args, type(args))  
    return sum(args)  
  
result = add(10,20,30,40,50)  
print(result)

Output Response -
(10, 20, 30, 40, 50) <class 'tuple'>
150
```

- Star ( * ) will alow to take multiple values
- Args [ args ] will store all these values as a tuple

- If we don't give any number of arguments, it means args will have 0 elements
- It will be still a tuple
- Below the example of 0 arguments passed.
```
def add(*args):  
    print(args, type(args))  
    return sum(args)  
  
result = add()  
print(result)

Output Response -
() <class 'tuple'>
0
```

- If we any situation or a condition where we don't know how many number of arguments that a function  should take, we can use * args. [ * args ]
- One more thing about ( args ), we have to understand ( args ) is a standard, not a mandatory thing
	- It means instead of args, i can use an another variable
```
def add(*nums):  
    print(nums, type(nums))  
    return sum(nums)  
  
result = add(10,20)  
print(result)

Output Response -
(10, 20) <class 'tuple'>
30
```

- args is a standard way. Its a PEP standard to be used in Python.
- What is PEP standard
	- There are lot of standard or convention written by Python developers to be used.
	- This is one of them
	- Technically, nums can be used or any variable x,y,z can be used instead of args
	- But * args is something when we see, we understand that this is used for variable lenght argument

```
def student_details(sid, sname, *marks):  
    if len(marks) == 0:  
        print(f"{sname} with id {sid} was absent in all the exams")  
    else:  
        percent = sum(marks)/len(marks)  
        print(f"{sname} with id {sid} secured {percent}%")  
  
student_details(101, "Shree", 20, 30, 40, 50)  
student_details(201, "Nidhi", 30, 40, 50, 60, 70, 80)  
student_details(301, "Sharma", 40, 50)  
student_details(401, "Nag")

Output Response -
Shree with id 101 secured 35.0%
Nidhi with id 201 secured 55.0%
Sharma with id 301 secured 45.0%
Nag with id 401 was absent in all the exams
```

---
---
