
- In previous section, we saw what are exceptions and how to handle exceptions using the Try and Except blocks

- Else
	- When the try statement does not raise the exception[when there is no error/exception in the try block]
		- The code enters the block called Else [Its kind of a fallback option where if there is no error happens in the try block, if we want to do something, we can do that in else block]

```
5-File1.txt
This file is created using the 'x' mode in Python  
Have a nice day!  
 This content has been written using 'a' mode   
'a' mode is used to add new content at the end of the file   
Good Bye!
```

```
try:  
    with open("5-File1.txt", "rt") as file_handler:  
        data = file_handler.read()  
except FileNotFoundError as file_error:  
    print("File that you are trying to open does not exist!")  
    print(file_error)  
else:  
    print(data)
    
Output Response -
This file is created using the 'x' mode in Python
Have a nice day!
 This content has been written using 'a' mode 
'a' mode is used to add new content at the end of the file 
Good Bye!
```


----
----

- Finally
	- Finally block is always executed irrespective of whatever the error happens or the exception is raised or not in the python.

- Else and Finally are optional
- Try and Except is mandatory to handle file handling errors


```
import io  
try:  
    fh = open("test.txt", "wt")  
    fh.write("hello world")  
except FileNotFoundError as file_error:  
    print("File that you are trying to open does not exist!")  
    print(file_error)  
except io.UnsupportedOperation as io_error:  
    print(io_error)  
# else:  
#     print("else block")  
#     # print(data)  
finally:  
    print("Finally statement")  
    fh.close()
    
Output Response -
Finally statement
```


---
---
