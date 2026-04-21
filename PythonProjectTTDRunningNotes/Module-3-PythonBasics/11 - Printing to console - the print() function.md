
Lets open up the IDLE shell
Until now, we used to write for example 
num1 = 100  : assigning the value 100 to the variable num1
num1 : once assigned, to display the output on the screen.

This way work in the IDE(Integrated Development Environment) which is interactive.
Example - IDLE Shell [This is an  interactive IDC. We are inside Python console]
- Here if the value is assigned to any variable, then if we just write the variable name in the next line, it would print the value that is assigned to the variable

But ideally in Python, if we want to display or print anything on the output screen/console - we need to use the function called Print()

In python, we usually write programs in dot py (.py) extension
We create files in .py extension, then we write the entire login in the file and to display the output of the logic, we write the print() function.

```
num1 = 100
print(num1)
100
```

Any function in python, in general the parenthesis needs to be opened and closed.
Example - print()

Print Single Value/Variable in the Output

```
name = "Shree"
print(name)
Shree
age = 29
print(age)
29
```

Print Multiple Values/Variable in the Output
The comma separated multiple values can be printed using the print function, but in the output there would be a space b/w output values.
Reason is that the print() function introduces a separator when more than 1 value/variable is being printed [to enhance the readability of the output]

```
name = "Shree"
print(name)
Shree
age = 29
print(age)
29
print(name,age)
Shree 29
print(10,20,30,40)
10 20 30 40 [ All of them have spaces in the middle] - This is called the Seperater
```

Question
- Is it by default the space is provided as a separator when more than one value is printed?
Answer
- Yes by default the value of separator is space [ " " ]

Question
- Can i change this separator?
Answer
* Yes, below is the example on how to do that.
	* Assume i need the output like this  --  10,20,30,40 [separated by commas]
		* print(10,20,30,40,sep=",")
	* One another thing to note here is after the last value, the separator will not be printed
		* Because separator is separate the values - it should be in the middle of the 2 values
			* After 40, there is no value, hence no separator after 40
	* Any valid string/character can be used as a separator.

```
print(10,20,30,40)
10 20 30 40

print(10,20,30,40,sep=",") instead of space as a seperator, comma becomes the seperator of all values
10,20,30,40

print(10,20,30,40,sep="#")
10#20#30#40

print(10,20,30,40,sep="Hi")
10Hi20Hi30Hi40
```


----

If we start the string with double quotes, then we have to end it double quotes
If we start the string with double quotes, then we end it with single quote, then it ends up with a syntax error.

```
print("Python")
Python

print("Python')    
SyntaxError: unterminated string literal (detected at line 1)
```

----

Including the strings/characters and the variable values in the print statement

```
num1 = 100
num2 = 200
result = num1 + num2
# Addition of 100 and 200 is 300
print("Addition of",num1, "and",num2, "is", result)
Addition of 100 and 200 is 300
```

```
name = "Shree"
age = 29
# Name: Shree Age:29     
print("Name:",name,"Age:",age)
Name: Shree Age: 29
```

```
day = 10     
month = 3
year = 2020
#10/3/2020
print(day,month,year,sep="/")
10/3/2020
```

---
