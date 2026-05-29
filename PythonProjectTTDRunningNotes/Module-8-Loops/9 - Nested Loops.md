
- In previous sections, we looked at FOR loops and WHILE loops.
- For loop - the loop that runs on a sequence
- While loop - its a condition based loop
- It can be run on string/list/tuple/set/dictionary or on a range function as well.
- In this section, we shall look what are Nested Loops
	- Nested loops are nothing but loops inside another loop
	- So its possible to write one loop inside another loop
		- We can write for loop inside while loop
		- We can write while loop inside for loop
		- We can write for loop inside for loop
		- We can write while loop inside while loop

For Loop inside For Loop

```
for i in range(3):  
    for j in range(2):  
        print(f" i = {i}, j = {j}")
        
Output Response -
 i = 0, j = 0
 i = 0, j = 1
 i = 1, j = 0
 i = 1, j = 1
 i = 2, j = 0
 i = 2, j = 1
```

---
---
