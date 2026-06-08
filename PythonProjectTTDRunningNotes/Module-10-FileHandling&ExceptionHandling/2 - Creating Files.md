
- This section, we shall see how to create a file
	- create a file - x mode  
		- if the file doesn't exist, it will create a file. 
		- fh = open("file1.txt", "xt")
	- once we create a file, we write some content in it.

```
# create a file - x mode  
# if the file doesn't exist, it will create a file.  
fh = open("file1.txt", "xt")  
  
# writing into a file  
# write(content)  
fh.write("This file is created using the 'x' mode in Python \n Second line" )  
fh.write("\nThird line")  
  
# closing the file  
fh.close()

Output Response

```


- file "file1.txt" has been created with the content provided above
	- This file is created using the 'x' mode in Python   
	-  Second line  
	- Third line

---

- After closing the file, we cannot write the content in the file again, we will get error
```
##### ERROR  
  
# create a file - x mode  
# if the file doesn't exist, it will create a file.  
fh = open("file1.txt", "xt")  
  
# writing into a file  
# write(content)  
fh.write("This file is created using the 'x' mode in Python \n Second line" )  
fh.write("\nThird line")  
  
# closing the file  
fh.close()  
  
# write after closing the file will result in error  
fh = write("Write after closing the file")

Output Response -
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\10-File&ExceptionHandling\2-CreatingFiles.py", line 19, in <module>
    fh = open("file1.txt", "xt")
FileExistsError: [Errno 17] File exists: 'file1.txt'
```

- If the file already exists, we cannot create it again

----
---
