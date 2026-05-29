
- In this section, we shall look at 2 of the control statements which basically helps us to control our loops
	- Continue
	- Break

1. Continue
	1. Continue skips the statement which are present after the continue statement inside the loop and proceeds to the next loop or next iteration.
	2. Basically Continue statement gives control to the start of the loop, by skipping anything which is written below it.

```
-- Continue Statement
for num in range(10):  
    if num % 3 == 0:  # if the number is divisible by 3
        continue  
    print(num)
    
Output Response -
1
2
4
5
7
8
```

In the above example
- The range will start from 0
- The range will stop before 10 i.e at 9
- The range will have the step as 1
	- The range will be 0,1,2,3,4,5,6,7,8,9
- The 1st value of num is 0
	- 0 % 3 == 0
		- Answer is Yes
			- So it will continue
				- It means the program control goes to the for loop, anything below "continue" will not be printed.
				- Continue makes all the statements/all the lines of code written below it to skip
- The 2nd value of num is 1
	- 1 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go the print function and prints the number
			- print(num)
				- In our case 1 will be printed at the output
- The 3rd value of num is 2
	- 2 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go to the print function and prints the number
			- print(num)
				- In our case 2 will be printed at the output
- The 4th value of num is 3
	- 3 % 3 == 0
		- Answer is Yes
			- So it will continue
				- It means the program control goes to the for loop, anything below "continue" will not be printed
				- Continue makes all the statements/all the lines of code written below it to skip
- The 5th value of num is 4
	- 4 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go to the print function and prints the number
			- print(num)
				- In our case 4 will be printed at the output
- Similar way for the values 6 and 9
	- 6 % 3 == 0 and 9 % 3 == 0
		- Answer is Yes
			- So it will continue
				- It means the program control goes to the for loop, anything below "continue" will not be printed
				- Continue makes all the statements/all the lines of code written below it to skip
- Similar way for the values 5,7,8
	- 5 % 3 == 0 and 7 % 3 == 0 and 8 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go to the print function and prints the number
			- print(num)
				- In our case 5,7,8 will be printed at the output

---
---

There is another keyword/statement called "Break"
Instead of "continue" if i use "break" - then what would happen?

2. Break
	1. Break is a statement which basically makes the control go out of the loop when it encounters the break statement
		1. It terminates or exits the loop

```
-- Break Statement
for num in range(1, 10):  
    if num % 3 == 0:  
        break  
    print(num)
    
Output Response -
1
2   
```

In the above example
- The range will start from 1
- The range will stop before 10 i.e at 9
- The range will have the step as 1
	- The range will be 1,2
- The 1st value of num is 1
	- 1 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go to the print function and prints the number
			- print(num)
				- In our case 1 will be printed at the output
- The 2nd value of num is 2
	- 1 % 3 == 0
		- Answer is No
			- So it will not go inside the if block
			- Instead it will go to the print function and prints the number
			- print(num)
				- In our case 2 will be printed at the output
		- Answer is No
			- So it will continue
				- It means the program control goes to the for loop, anything below "continue" will not be printed.
				- Continue makes all the statements/all the lines of code written below it to skip
- The 3nd value of num is 3
	- 3 % 3 == 0
		- Answer is Yes
			- So it will go inside the if block
				- And it encounters the break statement
					- Break statement terminates the loop i.e it goes out of the loop itself
					- And after the loop we don't have anything in the program, so nothing gets printed.
				- So it will not go through the other elements/items in the range
					- it doesn't go through 4, 5, 6, 7, 8, 9
				- It will directly break out of the loop as soon as the 1st iterated value encounters the break statement.