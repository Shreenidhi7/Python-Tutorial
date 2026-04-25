
fString is the way to format strings in python

What is the meaning of formatting string?
- When we have a string and we want to impute some values from a variable inside the sting we use the feature fString.

Lets take some example to understand how we fString in Python and what they are.

1. Basic Example of how we print the values of the variable
	1. Below is the normal/usual way to print the values of variables
		1. This is suggested when we have limited variables to print. 
```
name = "Shree"  
age = 29  
language = "Python"  
hours = 3
  
# Shree is 29 years old  
print(name,"is",age,"years old")

# Shree is 29 years old. He studies Python 3 hours a day  
print(name,"is",age,"years old. He studies",language,hours,"a day")

Output Response -
Shree is 29 years old
Shree is 29 years old. He studies Python 3 a day
```


2. When we have a lot of variables (like 10) that needs to be imputed, the above method is bit hectic[adding variable in the sentence in the print statement]
	1. This is where the feature of fString in Python comes into picture.
		1. Wherever there is a variable, we use curly brackets[{}] and we put the variable inside it.
		2. It will be a single string [there won't be any commas, plus sign]
			1. Its not separated by commas, plus sign in the print function.
		3. Another thing to note here is that we need to mention "f" in front of the string statement in print function
			1. It a way to tell python that whatever we are using in curly brackets needs to be imputed/fetched the value of variables
		4. # Using fString  
			1. print(f"{name} is {age} years old. He studies {language} {hours} a day")

```
name = "Shree"  
age = 29  
language = "Python"  
hours = 3
  
# Shree is 29 years old  
print(name,"is",age,"years old")

# Shree is 29 years old. He studies Python 3 hours a day  
print(name,"is",age,"years old. He studies",language,hours,"a day")

# Using fString  
print(f"{name} is {age} years old. He studies {language} {hours} a day")

Output Response -
Shree is 29 years old
Shree is 29 years old. He studies Python 3 a day
Shree is 29 years old. He studies Python 3 a day
```

---

Few more examples on this.
1. Lets say we have a variable called sub1 = 78, sub2 =87, sub3 =83
2. Create a variable called total -> adding all sub1+sub2+sub3
3. Also have a print function where you add sub1+sub2+sub3
4. We have to print -> Shree scored {total} marks in total
5. We have to print -> Shree scored {sub1+sub2+sub3} in total

```
name = "Shree"
sub1 = 78  
sub2 = 87  
sub3 = 83  
total = sub1 + sub2 + sub3  
print(f"{name} scored {total} marks in total")  
print(f"{name} scored {sub1+sub2+sub3} marks in total")

Output Response -
Shree scored 248 marks in total
Shree scored 248 marks in total
```

---

If we have not provided "f" at the starting of the print statement, then the variable values wont be imputed/fetched in the print statement
Only writing the variables under curly braces wont work - we need to have "f" in the print statement.

```
name = "Shree"
sub1 = 78  
sub2 = 87  
sub3 = 83
percent = (sub1 + sub2 + sub3)/100

#Without fString
print("{name} scored {percent:.2f}% in total")
Output Response -
{name} scored {percent:.2f}% in total

#With fString
print(f"{name} scored {percent:.2f}% in total")
Output Response -
Shree scored 2.48% in total
```


---

This behavior is only possible with the string data types, that's the reason its called fString

---
