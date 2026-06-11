
- This section we will look at how to append or add any new content into an existing file
- For this purpose, we will use 'a' mode which is nothing but Append Mode
	- If appends/add a content to the end of the file.

- The below example is considered when the "5-File1.txt" exists/present in the folder

```
5-File1.txt
This file is created using the 'x' mode in Python  
Have a nice day!
```

```
5-AppendingIntoAFile.py

# 'a' mode => append mode  
  
file_handler = open("5-File1.txt", 'a+t' )  
file_handler.write("\n This content has been written using 'a' mode \n")  
file_handler.write("'a' mode is used to add new content at the end of the file \n")  
file_handler.write("Good Bye!")  
file_handler.close()

Output Response -
This file is created using the 'x' mode in Python  
Have a nice day!  
 This content has been written using 'a' mode   
'a' mode is used to add new content at the end of the file   
Good Bye!
```

---

- The below example is considered when the file doesn't exist.
	- If the file doesn't exist, 'a' mode creates a the file
- The main difference between 'w' mode and 'a' mode is that 'a' mode doesn't truncate any content of the existing file. It adds the contents at the end of the file rather than deleting them.
- On the other hand, 'w' mode deletes the content of an existing file if used on an existing file and overwrites those contents
- If used with a new file, 'w' mode creates that file and writes the content similar to a mode
	- 'a' mode also creates a file if a file doesn't exist.

```
5-AppendingIntoAFile.py
  
file_handler = open("5-File2.txt", 'a+t' )  
file_handler.write("This content has been created using 'a' mode \n")  
file_handler.write("'a' mode creates a file, if the file doesn't exist \n")  
file_handler.write("Good Bye!")  
file_handler.close()

```

```
This content has been created using 'a' mode   
'a' mode creates a file, if the file doesn't exist   
Good Bye!
```

----
---

- 'r' mode - read the content of the file
- read() - read the entire content as a string
- read(n) - read n number of characters of the string
- readlines() - read all the content of the file as lines
- readline() - read each line at a time
- 'x' mode - used to create a file
	- if file exists, 'x' mode will give an error
- 'w' mode - can be used to create file, but mostly used to overwrite/change the contents of the file
	- if 'w' mode is used for the file that doesn't exist, it will create a file
- 'a' mode - appends new contents at the end of the file.
	- if 'a' mode is used for the file that doesn't exist, it will also create a file
- r, read(), readlines(), readline()
	- all these are reading functions
- x, w, a 
	- all these are writing functions

---
---
