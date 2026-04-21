
This section, we shall learn about another function in Python.
Its called Input Function

In last section, we learnt about the print function, which is used to display/print the output or any value/variable's value on the screen.
In input function, as the name suggest is used to take an input from the user.

Till now, we were just assigning values to a variable - This is called hard coding.
So now, for example if we have to write a program in which we don't have the value for the variable [Example : name = "Shree"] (Assume we don't know the name of the person)
Rather, we need to ask the user for the name that as to be assigned to a variable.

In Python or any other programming language, if we have to take an input from the user, there has to be a way otherwise the program will not be able to interact with the user.
In Python, we have the **input function** to interact with the user or to take inputs from the user.

Input Function will give an option for the user to write some values.

---

How to User Input Function?
- In Python's IDLE, write the below
	- first_name = input() and press enter
		- When we run the above program, we can observe the cursor is blinking, it means its waiting for us to type the input value
		- We type "Shree" and press enter, the value "Shree" will get stored in the variable "first_name"
			- So now, how do we verify whether the value is stored or not?
				- We can verify by printing the variable name
					- print(first_name)
						- Shree
		- This means using the input() [input function], we have typed in the value for the variable first_name and we have stored the value ["Shree"] in the variable [first_name]

```
#Input Function
      
first_name = input()
Shree
print(first_name)
Shree

age = input()    
29
print(age)
29
```

---

In the above example, when we say input(), how would the user know that he has to provide the input as name? Since we are writing the program, we created a variable first_name hence we knew that name should be provided as input. Same with age.
- But when we write program, the end user might not be able to understand what the program actually expects the user to provide as a input

In order to bridge this gap, we need to educate/inform/tell the user what value the user is expected to provide in the input section
- It can be done by using an option called "Prompt" in the input function.
	- Lets re-write the program with the prompt or with the message that tells the user what to insert/input.
		- Whatever the statement we write in the input function's prompt, that would be displayed to the user, so that he could act according to the message/statement from the prompt

```
first_name = input("Enter your name: ")
Enter your name: Shree

age = input("Enter your age: ")
Enter your age: 29

print(first_name, age)
Shree 29
```

Learnings - Instead of hard coding the values, we could take inputs from the user using the input function [ input() ]

----

Lets write a simple program wherein we take 2 numbers form the user and try to add them and display the result using the print function.

```
num1 = input("Enter a number: ")    
Enter a number: 10
num2 = input("Enter another number: ")
Enter another number: 15
print(num1)
10
print(num2)
15
result = num1 + num2
print(result)
1015

# Verification of the data type
type(num1)
<class 'str'>

type(num2)
<class 'str'>

type(result)
<class 'str'>

#String Concatenation is Performed here instead of Numerical Addition.

```

We were expecting 25 as the output, but the output observed is 1015.
Why has this happened?
- Here is one important thing we have to understand about the input function.
	- When we use the input function and receive/fetch an input from the user, it will be received as a String and stored as a String in the variable.
		- How do we verify that?
			- We can use a type function and confirm the type of the input and the output.
			- num1 is str
			- num2 is str
				- num1 and num2 here is not an addition but a string concatenation, due to this the result of num1 and num2 is also a string


---

Think how this can solved?
Solution
- We have already understood the concept of typecasting/type conversion.
- We can change the data type of num1 & num2 from string to integer.
	- There are many approaches that can be followed
		- Below are some example

```
# Approach - 1 [Type Casting at Result Level]
num1 = (input("Enter a number: "))    
Enter a number: 10

num2 = (input("Enter another number: "))
Enter another number: 15

print(num1)
10

print(num2)      
15

result = int(num1) + int(num2)
print(result)
25
print(type(result))
<class 'int'>
```


```
# Approach - 2 [Type Casting at Input Level]
num1 = int(input("Enter a number: "))    
Enter a number: 10

num2 = int(input("Enter another number: "))
Enter another number: 15

print(num1)
10
print(type(num1))
<class 'int'>

print(num2)      
15
print(type(num2))
<class 'int'>

result = num1 + num2   
print(result)
25
print(type(result))
<class 'int'>
```

---

Learnings - Input function always gives us String.
Depending on the data type that  we are expecting, we need to convert/typecast to the required data type
We always get a string, if we are expecting an integer, we will typecast it into an integer
if we are expecting a float, we will typecast it into a float and so on.
