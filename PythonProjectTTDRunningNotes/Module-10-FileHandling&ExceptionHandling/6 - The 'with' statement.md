
- This section, we will look at what is 'with' statement and how it can used with file handling and what are the advantages of with statement in file handling.
- The 'with' statement is python simplifies the resource management by automatically handling the setup and cleanup task
- It basically ensures that the resources are properly release even though there are errors in the code
	- It makes the code clean

- When we work with files, its important to close the file properly and even open the files without any issues


- Regular way to open and close the file

```
6-Practice1.txt

This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
filehandler = open("6-Practice1.txt","rt")  
contents = filehandler.read()  
print(contents)  
filehandler.close()

Output Response -
This is a test file
We are learning file handling in python
Modes to open a file are: r, w, a, x, t, b.
```


---

- Using 'with' statement, opening, performing actions and closing the file.


```
6-Practice1.txt

This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
with open("6-Practice1.txt") as fileHandler:  
    contents = fileHandler.read()  
  
print(contents)

Output Response -
This is a test file
We are learning file handling in python
Modes to open a file are: r, w, a, x, t, b.
```

- Here 'with' statement ensure it automatically closes the files 

- Another example

```
with open("6-Practice2.txt", "xt") as fileHandler:  
    fileHandler.write("This file has been created using Python \n")  
    fileHandler.write("Bye")
```

```
6-Practice2.txt
This file has been created using Python   
Bye
```

- Even though there is an error while reading/writing the file, the 'with' statement will close the file before terminating ensuring the rightful way to handle the error.

---
---
