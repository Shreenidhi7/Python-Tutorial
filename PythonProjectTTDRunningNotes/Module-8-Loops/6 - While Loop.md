
- In this section, we shall discuss about while loops
- There is another kind of loop in python apart from FOR LOOP that is called WHILE LOOP.
	- A While Loop executes a block of statement repeatedly until a given condition is TRUE
		- While loop terminates when the condition given becomes false.
- In case of FOR LOOP, we have a fixed list or fixed tuple or a fixed length of strings.
	- We know the length of it and the FOR LOOP runs for those many number of times.
	- Even in the case of range, we specify the interval in which we want to generate a number, so FOR LOOP runs those many number of times.
- In case of WHILE LOOP, it depends on the condition and that's the reason its called **"conditional based loop"**
	- It will keep on doing the same thing again and again until the condition is TRUE
	- And when the condition becomes FALSE, the control comes out of the loop and executes the rest of the program.
- Syntax of while loop
	- while condition:
		- statements

Major Difference b/w IF and WHILE
- IF -> Its is something that run once
	- When the condition is TRUE, the statements will run only once.
- WHILE -> It keeps on executing the statements written inside the while block until the condition is True and when it becomes False, it comes out.

FOR LOOP
```
for i in range(1, 5, 1):  
    print(i)
    
Output Response -
1
2
3
4
```

WHILE LOOP
```
num = 1  
while num < 5:  
    print(num)  
    num = num + 1
    
Output Response -
1
2
3
4
```

Important thing to note
- Its mandatory to add the line => num = num + 1
	- If we don't add this, then the while loop will become an infinite loop.
		- Infinite loop is a loop which doesn't stop.

----
----
