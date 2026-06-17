
- This section, we will look at methods to check if a file exists or not using Python
- There are multiple ways to verify the existence of a file in Python

1.  os.path.exists()
	1. The exists() is part of the OS module
	2. Its a straightforward way of checking if the file exists or not.
	3. We need to import the OS module
		1. We can provide a file path/file name

```
7-Practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
# os.path.exists()  
  
import os  
file_name = "7-Practice.txt"   
if os.path.exists(file_name):  
    print("File Exists")  
else:  
    print("File Does Not Exist")

Output Response -
File Exists
```

- We can also use full path
	- The full path can be taken by hovering on the file name or right click on the file and go to the option called "Copy Path/Reference" and select option "Absolute Path"

```
import os
file_name = "D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\7-Practice.txt" 
if os.path.exists(file_name):  
    print("File Exists")  
else:  
    print("File Does Not Exist")

Output Response -
D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\7-CheckIfAFileExists.py:11: SyntaxWarning: "\P" is an invalid escape sequence. Such sequences will not work in the future. Did you mean "\\P"? A raw string is also an option.
  file_name = "D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\7-Practice.txt"
File Does Not Exist
```

- There is an error when we select an absolute file path
	- This is because of the backslash
		- Backslash is used in case of a special character line \n or \t in python.
	- Instead of backslash, we could provide frontslash [ / ] at all the places.

```
import os
file_name = "D:/Python/PythonTTDTutorial/10-File&ExceptionHandling/7-Practice.txt" 
if os.path.exists(file_name):  
    print("File Exists")  
else:  
    print("File Does Not Exist")

Output Response -
File Exists

```


----

- Second way is to use the 'pathlib.Path.exists()' 
	- module is pathlib
	- function is Path.exists()

```
from pathlib import Path  
  
file_name = Path("D:/Python/PythonTTDTutorial/10-File&ExceptionHandling/7-Practice.txt")  
if file_name.exists():  
    print("File Exists")  
else:  
    print("File Not Exists")

Output Response -
File Exists

```


---

- If we want to create a file
	- Avoiding the error by checking if file exists

```
from pathlib import Path  
file_name = Path("D:/Python/PythonTTDTutorial/10-File&ExceptionHandling/7-Practice1.txt")  
if file_name.exists():  
    print("File Exists. Cannot Create")  
else:  
    print("File Doesnot Exists, Creating It")  
    file_handler = open(file_name, "xt")  
    file_handler.write("new content")  
    file_handler.close()

Output Response -
File Doesnot Exists, Creating It
```

```
7-Practice1.txt

new content
```


----
