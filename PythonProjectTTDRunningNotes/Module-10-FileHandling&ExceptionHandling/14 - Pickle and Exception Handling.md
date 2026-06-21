
```
import pickle  
  
students = {  
    'student1': {'roll': 101, 'name' : 'John', 'percent' : 78.5},  
    'student2': {'roll': 102, 'name' : 'Michael', 'percent' : 97.5},  
    'student3': {'roll': 103, 'name' : 'Shreenidhi', 'percent' : 97.5},  
}  
  
print(students)  
print(type(students))  
  
# Serilization  
with open("14-StudentsInformation.bin", "bw") as file_handler:  
    for student in students:  
        pickle.dump(students[student], file_handler)  
  
studentsMarksGreterThan90 = []  
# DeSerilization  
# Print the name of students who secured 90 or more marks  
with open("14-StudentsInformation.bin", "rb") as file_handler:  
    while True:  
        try:  
            data = pickle.load(file_handler)  
            if data["percent"] >= 90:  
                studentsMarksGreterThan90.append(data["name"])  
        except EOFError:  
            print("Done")  
            break  
print(f"Students with marks 90 or more : {studentsMarksGreterThan90}")

Output Response - 
{'student1': {'roll': 101, 'name': 'John', 'percent': 78.5}, 'student2': {'roll': 102, 'name': 'Michael', 'percent': 97.5}, 'student3': {'roll': 103, 'name': 'Shreenidhi', 'percent': 97.5}}
<class 'dict'>
Done
Students with marks 90 or more : ['Michael', 'Shreenidhi']
```

