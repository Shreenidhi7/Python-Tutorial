
- This lecture, we shall look at the "w" mode
- The 'w' in file handling is to open the file for writing.
	- It basically truncates the contents of the file or overwrites the file.
- The 'w' mode needs to used carefully as the 'w' mode overwrite the content of the existing file.
- The changes cannot be reverted, the existing file contents will be lost.

- The below example is when the file exists
```
# w mode - open the file for writing.  
## Its overwrites the file  
  
fh = open("3-file2.txt", "wt")  
fh.write("This file is overwritten using 'w' mode in Python - New Content\n")  
fh.write("Have a nice day!, New Content")  
fh.close()

Output Response -

```

```
3-file2.txt
This file is overwritten using 'w' mode in Python - New Content  
Have a nice day!, New Content
```

---

- The above example is when the file already exists, but what if just run the code and the file doen't exist in the system.
	- If the file doesn't exist, the 'w' mode will create a new file.

- If we use 'x' mode on the existing file, it will give error.
- The reason is that, 'x' mode will only look for new files to be created.
	- If the file exists with same name and we use 'x' mode to create a file, then there would be an error.
- But 'w' can work in both cases
	- If the files doesn't exist, then 'w' mode will create a new file
	- If the file exist, then 'w' mode will be used to update the existing file.

```
fh = open("3-file3.txt", "wt")  
fh.write("This file is overwritten using 'w' mode in Python \n")  
fh.write("Have a nice day!,")  
fh.close()

Output Response -

```

```
3-file3.txt

This file is overwritten using 'w' mode in Python   
Have a nice day!,
```

---
---

- Its better to use 'x' mode to create a file - safe way to do it.
- Its better to use 'w' mode to update an existing file