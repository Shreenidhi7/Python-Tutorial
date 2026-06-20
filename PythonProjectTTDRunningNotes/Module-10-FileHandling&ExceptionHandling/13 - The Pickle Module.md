
- In this module, we shall look into the pickle module
- We shall go through the serialization and deserialization on common data types in python like lists and dictionaries
- Why and how to use Pickle Module?

- In python, we work with high level data type like lists, tuples, sets and dictionaries and when we want to store these data types in memory or in files, they need to be converted into sequence of bytes that the computer can understand
	- This process is called serialization
- When we want to access these data structures back from the file that we have stored, these sequence of bytes are stored in the sequence of bytes must be converted back to the original data type
	- This process is called de-serialization


- Problem Statement

```
students = {  
    'student1': {'roll': 101, 'name' : 'John', 'percent' : 78.5},  
    'student2': {'roll': 102, 'name' : 'Michael', 'percent' : 97.5},  
    'student3': {'roll': 103, 'name' : 'Michael', 'percent' : 97.5},  
}  
  
print(students)  
print(type(students))  
  
# with open('13-StudentsInfo.txt', 'wt') as file_handler:  
#     file_handler.write(students)  
  
with open('13-StudentsInfo.txt', 'rt') as file_handler:  
    content = file_handler.read()  
  
print(type(content))  
output = dict(content)  
print(output)

Output Response -
{'student1': {'roll': 101, 'name': 'John', 'percent': 78.5}, 'student2': {'roll': 102, 'name': 'Michael', 'percent': 97.5}, 'student3': {'roll': 103, 'name': 'Michael', 'percent': 97.5}}
<class 'dict'>
<class 'str'>
{}
```

---

Soluttion to Problem Statement

```
import pickle  
  
students = {  
    'student1': {'roll': 101, 'name' : 'John', 'percent' : 78.5},  
    'student2': {'roll': 102, 'name' : 'Michael', 'percent' : 97.5},  
    'student3': {'roll': 103, 'name' : 'Michael', 'percent' : 97.5},  
}  
  
print(students)  
print(type(students))  
  
# Serialization  
with open('13-students.bin', 'bw') as file_handler:  
    for student in students:  
        pickle.dump(students[student], file_handler)  
  
# De-Serialization  
with open('13-students.bin', 'rb') as file_handler:  
    data1 = pickle.load(file_handler)  
    print(data1, type(data1))  
    data2 = pickle.load(file_handler)  
    print(data2, type(data2))  
    data3 = pickle.load(file_handler)  
    print(data3, type(data3))
    
Output Response -
{'student1': {'roll': 101, 'name': 'John', 'percent': 78.5}, 'student2': {'roll': 102, 'name': 'Michael', 'percent': 97.5}, 'student3': {'roll': 103, 'name': 'Michael', 'percent': 97.5}}
<class 'dict'>
{'roll': 101, 'name': 'John', 'percent': 78.5} <class 'dict'>
{'roll': 102, 'name': 'Michael', 'percent': 97.5} <class 'dict'>
{'roll': 103, 'name': 'Michael', 'percent': 97.5} <class 'dict'>
```


