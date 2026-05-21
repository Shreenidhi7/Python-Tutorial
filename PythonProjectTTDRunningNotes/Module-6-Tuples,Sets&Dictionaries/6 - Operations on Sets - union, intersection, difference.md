
- In this section, we shall discuss about the operations on sets, basically the operations which are mathematical
	- Python Sets are similar to the sets in mathematics
- There are certain operations that we can perform with mathematical sets like union, intersection, difference...
	- These operations are supported in Python as well.

Examples
- There are 2 students and they study certain subjects and they are stored as part of set.

Intersection Operation 
- If we want to find the common subjects within the 2 students, then we can use "Intersection" function or "&" operator
```
student1 = {"English", "Maths", "CS", "Chemistry", "Physics"}  
student2 = {"English", "Biology", "Chemistry", "Physics"}  
student3 = {"Sanskrit", "Maths", "CS"}
  
# common subjects of student1 and student2  
  
print(f"subjects of student1 : {student1}, and type of student1 : {type(student1)}")  
print(f"subjects of student2 : {student2}, and type of student2 : {type(student2)}")  
# common_subjects = student1.intersection(student2)  
common_subjects = student1 & student2  
print(f"common subjects of student1 and student2 : {common_subjects} and type of common_subjects : {type(common_subjects)}")
common_subjects_again = student1 | student2 | student3  
print(f"common subjects of student1, student2 and student3 : {common_subjects} and type of common_subjects : {type(common_subjects)}")

Output Response - 
subjects of student1 : {'Chemistry', 'Maths', 'Physics', 'CS', 'English'}, and type of student1 : <class 'set'>
subjects of student2 : {'Chemistry', 'Physics', 'English', 'Biology'}, and type of student2 : <class 'set'>
common subjects of student1 and student2 : {'Chemistry', 'Physics', 'English'} and type of common_subjects : <class 'set'>
common subjects of student1, student2 and student3 : set() and type of common_subjects : <class 'set'> 
```

If there is no common subject among all 3 sets, then the response will be "set()" => This is called an EMPTY SET

---

Union Operation
- If we want to find the all the subjects of student1 and student2 and student3, we can use the "Union" function or the "|" operator
```
student1 = {"English", "Maths", "CS", "Chemistry", "Physics"}  
student2 = {"English", "Biology", "Chemistry", "Physics"}  
student3 = {"Sanskrit", "Maths", "CS"}  
print(f"subjects of student1 : {student1}, and type of student1 : {type(student1)}")  
print(f"subjects of student2 : {student2}, and type of student2 : {type(student2)}")

Output Response - 
# all subjects of student1 and student2  
all_subjects = student1.union(student2, student3)  
# all_subjects = student1 | student2 | student3  
print(f"all subjects of student1 and student2 and student3 : {all_subjects} and type of all_subjects : {type(all_subjects)}")
```


---

Difference Operation
- If we want to find the difference b/w 2 sets, we can use "Difference" function.
	- Elements of set1 which are NOT in set2

```
# DIFFERENCE  
days = {"Mon", "Tue", "Wed", "Thur", "Fri", "Sat", "Sun"}  
weekends = {"Sat", "Sun"}  
  
weekdays = days.difference(weekends)  
weekdays_again =  days - weekends  
print(f"weekdays : {weekdays}")

Output Response - 
weekdays : {'Mon', 'Fri', 'Wed', 'Thur', 'Tue'}
```

---
---
