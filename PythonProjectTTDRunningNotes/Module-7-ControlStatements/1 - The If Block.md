
- This section we shall discuss about the conditional statements in Python
- Conditional Statements
	- As the name suggests, it has some conditions, it involves certain conditions
	- These are fundamental concepts of programming language that allow us to program - which is used to make decisions on a certain criteria/condition.
		- In Python we use something called if statement or if condition to basically control the execution flow or define a certain flow by writing condition and if the condition is true we do certain action depending on that.
		- Example - If somebody is 18 or above, they are called as adults and they can maybe cast their votes
			- If somebody is not 18, so they cannot cast their votes
		- We have seen the conditional or the relational operators which were
			- == , >=, <=, >, <, !=
			- These operators are actually used to define the condition which gives us in return Boolean values [True or False]
	- Syntax -
		- if condition:
			- block
				-  A block is a multiple line of code
		- once we complete writing the condition and and then press enter, it doesn't go the start of the line, but it leaves a space - this is called identation
		- Indentation - Its nothing but the spaces to create blocks in python
		- The standard for creating spaces or indentation in Python is 4 spaces
		- So if we see, automatically it gives us 4 spaces as indentation
		- Every block that we are going to see in python will have indentation including the if block.
		- if condition:
			- statement1
			- statement2
			- statementN
		- print()
		- -> if the condition is true, it will go inside the block, run the statements inside the blocks and after the block is completed, it will go out of the block and then it will run the print() statement
		-  -> if the condition is false, it will not go inside the block, it will directly go to the print() statement

```
# ==, >=, <=, >, <, !=  
# Syntax of if block  
###  
# if condition:  
#   statement1  
#   statement2  
#   statement3  
#   ...  
#   statementN  
# statementM  
###  
  
age = float(input("What is your age? "))  
if age >= 18:  
    print("Congrats! You are an Adult. You can now cast your vote")  
print("Reset of the program")

Output Response -
What is your age? 50
Congrats! You are an Adult. You can now cast your vote
Reset of the program

What is your age? 10
Reset of the program

```


----
---
