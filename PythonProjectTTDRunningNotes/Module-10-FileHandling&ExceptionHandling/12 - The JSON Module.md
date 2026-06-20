
- This section, we will see a python module called JSON
- Python's JSON module provides us with a utility that we need to effectively handle the JSON data
- JSON - Javascript Object Notation
	- Its widely used and accepted text format for data exchange.
	- The syntax of JSON resembles Python dictionaries
- JSON in python is handled using a very standard library called JSON.
	- JSON is very human readable format
- Straightforward Serialization and Deserialization can be done.
	- Usually JSON is used in API's and data storage.


- Serialization
	- dump()

```
import json  
students = {  
    'student1': { 'roll' : 123, 'name' : 'John', 'percent' : 98.5, 'sports' : True },  
    'student2': { 'roll' : 456, 'name' : 'Mark', 'percent' : 78.5 , 'sports' : False },  
    'student3': { 'roll' : 789, 'name' : 'Mark', 'percent' : 98.5 , 'sports' : True }  
}  
print(students)  
print(type(students))  
  
# dump  
with open("12-Students.json", "w") as file_handler:  
    json.dump(students, file_handler, indent=4)
    
Output Response -
{'student1': {'roll': 123, 'name': 'John', 'percent': 98.5, 'sports': True}, 'student2': {'roll': 456, 'name': 'Mark', 'percent': 78.5, 'sports': False}, 'student3': {'roll': 789, 'name': 'Mark', 'percent': 98.5, 'sports': True}}
<class 'dict'>
```

```
{  
    "student1": {  
        "roll": 123,  
        "name": "John",  
        "percent": 98.5,  
        "sports": true  
    },  
    "student2": {  
        "roll": 456,  
        "name": "Mark",  
        "percent": 78.5,  
        "sports": false  
    },  
    "student3": {  
        "roll": 789,  
        "name": "Mark",  
        "percent": 98.5,  
        "sports": true  
    }  
}
```


----
---

- De-Serialization
	- load()

```
12-Students.json
{  
    "student1": {  
        "roll": 123,  
        "name": "John",  
        "percent": 98.5,  
        "sports": true  
    },  
    "student2": {  
        "roll": 456,  
        "name": "Mark",  
        "percent": 78.5,  
        "sports": false  
    },  
    "student3": {  
        "roll": 789,  
        "name": "Mark",  
        "percent": 98.5,  
        "sports": true  
    }  
}
```


```
import json  
students = {  
    'student1': { 'roll' : 123, 'name' : 'John', 'percent' : 98.5, 'sports' : True },  
    'student2': { 'roll' : 456, 'name' : 'Mark', 'percent' : 78.5 , 'sports' : False },  
    'student3': { 'roll' : 789, 'name' : 'Mark', 'percent' : 98.5 , 'sports' : True }  
}  
print(students)  
print(type(students))  
   
# load  
with open("12-Students.json", "r") as file_handler:  
    data = json.load(file_handler)  
  
print(data)  
print(type(data))

Output Response -
{'student1': {'roll': 123, 'name': 'John', 'percent': 98.5, 'sports': True}, 'student2': {'roll': 456, 'name': 'Mark', 'percent': 78.5, 'sports': False}, 'student3': {'roll': 789, 'name': 'Mark', 'percent': 98.5, 'sports': True}}
<class 'dict'>
```


----
---

- Add/Append to Existing Data
	- Update function

```
{  
    "student1": {  
        "roll": 123,  
        "name": "John",  
        "percent": 98.5,  
        "sports": true  
    },  
    "student2": {  
        "roll": 456,  
        "name": "Mark",  
        "percent": 78.5,  
        "sports": false  
    },  
    "student3": {  
        "roll": 789,  
        "name": "Mark",  
        "percent": 98.5,  
        "sports": true  
    }  
}
```

```
import json
studentsUpdate = {  
    'student1': { 'roll' : 123, 'name' : 'Shree', 'percent' : 95.5, 'sports' : False },  
    'student2': { 'roll' : 456, 'name' : 'Mark', 'percent' : 78.5 , 'sports' : False },  
    'student3': { 'roll' : 789, 'name' : 'Mark', 'percent' : 98.5 , 'sports' : True }  
}  
  
# read the old data from the json file  
with open('12-Students.json', 'r') as file_handler:  
    data = json.load(file_handler)  
  
# update operation  
data.update(studentsUpdate)  
  
#dump - write the updated data in the json file  
with open('12-Students.json', 'w') as file_handler:  
    json.dump(data, file_handler, indent=4)
```

```
{  
    "student1": {  
        "roll": 123,  
        "name": "Shree",  
        "percent": 95.5,  
        "sports": false  
    },  
    "student2": {  
        "roll": 456,  
        "name": "Mark",  
        "percent": 78.5,  
        "sports": false  
    },  
    "student3": {  
        "roll": 789,  
        "name": "Mark",  
        "percent": 98.5,  
        "sports": true  
    }  
}
```


----
----

- Using Try-Except

```
import json
students = {  
    'student1': { 'roll' : 123, 'name' : 'John', 'percent' : 98.5, 'sports' : True },  
    'student2': { 'roll' : 456, 'name' : 'Mark', 'percent' : 78.5 , 'sports' : False },  
    'student3': { 'roll' : 789, 'name' : 'Mark', 'percent' : 98.5 , 'sports' : True }  
}  
  
studentsUpdate = {  
    'student1': { 'roll' : 123, 'name' : 'Shree', 'percent' : 95.5, 'sports' : False },  
    'student2': { 'roll' : 456, 'name' : 'Mark', 'percent' : 78.5 , 'sports' : False },  
    'student3': { 'roll' : 789, 'name' : 'Mark', 'percent' : 98.5 , 'sports' : True }  
}  
  
try:  
    # read the old data from the json file  
    with open('12-Students-1.json', 'r') as file_handler:  
        data = json.load(file_handler)  
except FileNotFoundError:  
    with open('12-Students-1.json', 'w') as file_handler:  
        json.dump(students, file_handler, indent=4)  
else:  
    # update operation  
    data.update(studentsUpdate)  
  
    #dump - write the updated data in the json file  
    with open('12-Students-1.json', 'w') as file_handler:  
        json.dump(students, file_handler, indent=4)
```


---
---
