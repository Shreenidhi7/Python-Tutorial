
- In previous section we looked at how to open and close a file.
	- There was an existing practice.txt created
- We opened that file in read and text mode and we closed it
- This section we will look at how to read the contents of the file.

- We already know how to open the file in text file, now we shall understand how to read a file.
- To read a file we have a function called "Read" function
	- If we open the file in text mode, read function reads the contents of the file as string
		- The entire content will be read as a string

```
4-practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
4-ReadingFiles.py
filehandler = open("4-practice.txt","rt")  
  
# read operation  
# read() => read the contents of the file as str  
content = filehandler.read()  

print(content)  
print(type(content))

# closing a file => close()  
filehandler.close()

Output Response -
This is a test file
We are learning file handling in python
Modes to open a file are: r, w, a, x, t, b.
<class 'str'>
```

- The above is to read the entire file.
	- The read function without providing anything in the paras, it will fetch/read everything in the file

---

- Instead of reading the entire content of the file, if we want to read certain number of characters from the file.
	- Lets say first 10 or 20 or 50 characters
		- content = filehandler.read(50)

```
4-practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
# read the character of the file  
# read operation  
# read() => read the contents of the file as str  
content = filehandler.read(50)  
  
print(content)  
print(type(content))  
  
# closing a file => close()  
filehandler.close()

Output Response -
This is a test file
We are learning file handling 
<class 'str'>
```


---

- There is another function or method by the name of "readline"
	- It is also used to read the content of the file.
	- But it reads the contents of the 1st line along with the '\n'

```
4-practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
# read the characters/contents of the file - using readline function/method  
# read operation  
# read() => read the contents of the file as str  
line1 = filehandler.readline()  
line2 = filehandler.readline()  
line3 = filehandler.readline()
line4 = filehandler.readline() #Empty String => the file has reached "End of File" (EOF)
  
print(f"Line 1: {line1}")  
print(f"Line 2: {line2}")  
print(f"Line 3: {line3}")
print(f"Line 3: {line4}")    
print(type(line1), type(line2), type(line3), type(line4))  
  
# closing a file => close()  
filehandler.close()

Output Response -
Line 1: This is a test file

Line 2: We are learning file handling in python

Line 3: Modes to open a file are: r, w, a, x, t, b.

Line 4: 
<class 'str'> <class 'str'> <class 'str'> <class 'str'> 
```

- We can notice that after Line 1 is printed there is a empty line printed as well
	- This is because, readline() method itself has already a "\n" pre-defined.

---

- There is another function called readlines()
	- It is similar to readline()
- But main difference is 
	- readline() -> it will read a single line at a time
	- readlines() -> it fetches all the lines together.

```
4-practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
# read all the lines together - readlines()  
# read operation  
# read() => read the contents of the file as str  
content = filehandler.readlines()  
  
print(f"Readlines Function Output - {content}")  
print(type(content))  
  
# closing a file => close()  
filehandler.close()

Output Response -
Readlines Function Output - ['This is a test file\n', 'We are learning file handling in python\n', 'Modes to open a file are: r, w, a, x, t, b.']
<class 'list'>
```

- print(content[0])  
- print(content[1])  
- print(content[2])

- This is a test file
- We are learning file handling in python
- Modes to open a file are: r, w, a, x, t, b.

```
4-practice.txt
This is a test file  
We are learning file handling in python  
Modes to open a file are: r, w, a, x, t, b.
```

```
# read all the lines together - readlines()  
# read operation  
# read() => read the contents of the file as str  
content = filehandler.readlines()  
  
for line in content:  
    print(line.rstrip("\n"), type(line))  
  
# closing a file => close()  
filehandler.close()

Output Response -
This is a test file <class 'str'>
We are learning file handling in python <class 'str'>
Modes to open a file are: r, w, a, x, t, b. <class 'str'>
```

---
---
