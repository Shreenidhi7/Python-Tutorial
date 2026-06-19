
- This section, we will look at how we can raise exceptions 
- As Python Developer, we ourselves can throw an exception if certain conditions are met or not.
- It allows us to interrupt the program based on the requirement or certain condition
- To throw an exception, we have use the keyword called raise

```
# raise  
salary = float(input("Enter your salary: "))  
if salary < 0:  
    raise ValueError("Your salary cannot be negative")  
else:  
    print(f"Your salary is {salary}")
    
Output Response -
Enter your salary: -1000
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\11-RaisingExceptions.py", line 6, in <module>
    raise ValueError("Your salary cannot be negative")
ValueError: Your salary cannot be negative
```

---

- Generic Exception also we could use
	- keyword is Exception
	- All exceptions or runtime errors come under this Exception
		- FileNotFoundError
		- io.UnsupportedOperation

```
age = float(input("What is your age = "))  
if age < 0:  
    raise Exception("Your age cannot be negative")  
else:  
    if age >= 18:  
        print("You are old enough to vote")  
    else:  
        print("You cannot vote")

Output Response -
What is your age = -10
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\11-RaisingExceptions.py", line 13, in <module>
    raise ValueError("Your age cannot be negative")
ValueError: Your age cannot be negative

Process finished with exit code 1
```

----
----
