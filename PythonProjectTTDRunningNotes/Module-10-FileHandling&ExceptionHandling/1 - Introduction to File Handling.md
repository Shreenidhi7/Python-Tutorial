
- This section, we will introduce ourselves something called File Handling in Python.
- We shall look at Files and how to handle them.
	- We know that data is very important and they are stored in files.
	- Every organizations like companies,schools,offices that depend on its data for continuing its business.
		- If the data is lost, organization will have losses.
	- We have store and handle data efficiently.
		- To store data in computer, we need files.
- When we want to deal with these files using a programming file like Python, we shall understand it in this section.
- In Python, basically Files gets classified and handled in 2 ways
	- Text Files
	- Binary Files
- Text Files are the files which store the data in form of characters
	- All the text characters if they are stored in a file that is treated as text file in Python.
- Binary Files are the files which store the data in form of bytes
	- Bytes = 8 bits
	- Binary files are basically the image files, audio and video files

- We shall majorly deal with the text files in this section
- Operations to be performed on a file
	- Read a file
	- Edit a file
	- Open a file
	- Create a file
	- Close a file
	- Delete contents of a file
	- Add new content to a file
	- Overwrite content to a file

- To perform read or write operation on a file, we need to open a file first.
	- Opening a file in Python  
	- open(file_name, mode_to_open)  
	- modes - 
		- r(read)
		- x(create)
		- w(write)
		- a(append)
		- t(text)
		- b(binary)
	- if we don't give also -> 'rt' will be the default mode
		- read and text
	- Using a file object/handler, we can perform any action on the file.

```
# Opening a file in Python  
  
# open(file_name, mode_to_open)  
# mode - r(read), x(create), w(write), a(append), t(text), b(binary)  
# if we don't give also -> 'rt' will be the default mode  
  
file_handler = open("practice.txt", "rt")  
print(file_handler)

Output Response -
<_io.TextIOWrapper name='practice.txt' mode='rt' encoding='cp1252'>
```

- <_io.TextIOWrapper name='practice.txt' mode='rt' encoding='cp1252'>
	- This means, its an file object or text io(input/ouput) wrapper and it is pointing to referring to file "practice.txt" and mode of file which is read/text mode
		- when we open the file, it will point to the beginning of the file
		- i.TextIOWrapper is nothing but the text object itself
		- This file object can used to perfrom task like read,write,append

```
# Opening a file in Python  
  
# open(file_name, mode_to_open)  
# mode - r(read), x(create), w(write), a(append), t(text), b(binary)  
# if we don't give also -> 'rt' will be the default mode  
  
file_handler = open("practice.txt", "rt")  
print(file_handler)  
#read operation  
  
#close a file  => close()  
file_handler.close()

Output Response -
<_io.TextIOWrapper name='practice.txt' mode='rt' encoding='cp1252'>
```

---

- practice.txt
	- This is a test file  
	- We are learning file handling in python  
	- Modes to open a file are: r, w, a, x, t, b.

---
