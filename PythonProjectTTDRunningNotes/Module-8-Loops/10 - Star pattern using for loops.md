
- Till now, we have learnt how to write for loops, while loops, nested loops and few examples around it.
- This section, we will try to write a python program to print the pattern.
- This pattern print stars [ * ]
```
*
* *
* * *
* * * *
* * * * *
```
- 1st line - it prints 1 star
- 2nd line - it prints 2 stars
- 3rd line - it prints 3 stars
- 4th line - it prints 4 stars
- 5th line - it prints 5 stars

- To write a program on it, we need to understand how to print this.
- Here for the above pattern,
	- The row numbers or the line number is equal to the number of stars that we want to print.
	- We need to print 5 lines, so for that we need to have a for loop
		- The outer loop is for 5 rows/5 lines and to control how many lines will be printed with each row.
	- We have to write inner loop for printing the stars
		- We have to write inner loop to control how many stars will be printed in each row.

- Important Note - By default the values in print() function will be printed in the next line after the execution of previous line execution
	- In order to avoid it, we can use the below parameter
		- print("*". end = " " )
	- If we want to go to the next line, we can directly use print()
		- print() [no need of \n - print() function alone will move the pointer to next line]

- So re-iterating
	- the outer loop -> "i" loop is for the number of rows/lines
		- so it has to go from 1 to 5
		- so we set the range - 1 to 6
	- the inner loop -> it runs "i" times for each row.
		- 1st row -> 1 star
		- 2nd row -> 2 stars
		- 3rd row -> 3 stars
		- 4th row -> 4 stars
		- 5th row -> 5 stars
	- The outer loop is to decide how many rows to print.
	- The inner loop decides how many starts to print in each row.
	- Since the number of stars is same as the row number/line number -> it has to go till "i" which is representing the row number
		- So the inner loop runs "i" times for each row
			- 1st row - 1 time
			- 2nd row - 2 times
			- 3rd row - 3 times
			- 4th row - 4 times
			- 5th row - 5 times
		- After printing the star [ * ] in that row, in the same row we don't want to go to the next line, so for that we provide [ end = " " ]
		- And after the inner loop is completed, i want to go to the next line, so for that we have used the print function - print()
	- So for the 1st row
		- j loop runs once, 1 star gets printed along with space after star
		- Then print() will take to the next line 
	- And i = 2
		- j runs twice
			- It will put 1st star * and then the second star *
				- * *
			- Its in the same line because of the [ end = " " ]
			- after it prints both the stars, we want to go to the next line
			- so print() will take to the next line
	- And i = 3 [same as above]
	- And i = 4 [same as above]
	- And i = 5 [same as above]


```
"""  
*  
* *  
* * *  
* * * *  
* * * * *  
  
"""  
  
for i in range(1,6):  
    for j in range(1,i+1):  
        print("*", end=" ")  
    print()
    
Output Response -
* 
* * 
* * * 
* * * * 
* * * * * 
```

----

Instead of printing stars [ * ], we could print "i" as well.

```
for i in range(1,6):  
    for j in range(1,i+1):  
        print(i, end=" ")  
    print()
    
Output Response -
1 
2 2 
3 3 3 
4 4 4 4 
5 5 5 5 5 
```

----
---
