
- In the last lecture, we discussed about the loops and how we can use loops for lists, dictionaries and strings. Same way we can use loops with Sets and Tuples.
- This lecture we shall learn about the range() function and how range function can be used with loops.

1. Range Function
	1. Range function is nothing but a built-in function in python.
	2. It is used to generate a sequence of integers
	3. Syntax =
		1. range(start, stop, step)
		2. Important thing to note is that it is similar to the slice function
			1. slice[1:2:3]
				1. Here the start is included
				2. Stop is not included
		3. The same is applied in the range() function as well
			1. The Stop is not included in the generation of the sequence that gets generated.
	4. Range also has 2 more syntax's
		1. range(start, stop) => step will be defaulted to 1
		2. range(stop) => 0 to stop-1 with th


Example of the Range() Function
- The 1st syntax of range() function
- Range function can be used with For Loop
	- for i in range(start, stop, step):
		- statements

```
for i in range(1, 10,1):  
    print(i)

Output Response -
1
2
3
4
5
6
7
8
9
```

- If we observe, it starts printing from 1,2,3,4,5,6,7,8,9
	- Start -> 1 -> Its included
	- Stop -> 10 -> Its not included
	- Step -> 1 -> The Step is 1
- If we want to include 10 as well, then Stop should be updated as 11.
- Now, instead of having Step as 1, If we update Step as 2.
	- After generating the 1st value, it will generate the value 2 steps ahead.

```
for i in range(1, 11,2):  
    print(i)

Output Response -
1
3
5
7
9
```

- We can say that we have just generated odd numbers between the numbers 1 and 10

Question
- Generate even numbers between 1 and 10 (10 excluded)
```
for i in range(2, 10,2):  
    print(i)
    
Output Response -
2
4
6
8
```

---

Question
- Generate numbers in the reverse order -> 20 to 10 (excluding 10)
```
# generate numbers in the reverse order : 20 to 10 (excluding 10)  
for i in range(20,10,-1):  
    print(i)

Output Response -
20
19
18
17
16
15
14
13
12
11
```

```
# generate numbers in the reverse order : 20 to 10 (excluding 10) - only even numbers  
for i in range(20,10,-2):  
    print(i)

Output Response -
20
18
16
14
12
```

---

- Similar example during a spacecraft or rocket going to space, we do a countdown.
- On the 0th count, we launch the rocket.

```
# countdown from 10 to 1 ( 1 included)  
for i in range(10,0,-1):  
    print(i)
    
Output Response -
10
9
8
7
6
5
4
3
2
1
Happy New Year
```


---
---

- Till now what we have seen that the range function has a start and a stop [the range in which we want to generate values] and then a step in which we want to generate values
- The next syntax is
	- range(start, stop) => step =1 by default
	- If we want to use the range function with the step as 1 by default, then we can use this range syntax
		- We can simple leave the step as blank, we don't have to put a comma after stop and mention any value.
		- If we don't give anything here, the step will be by default set to 1

```
for i in range(1,5):  
    print(i)
    
Output Response -
1
2
3
4
```


---
---

- The next syntax is 
	- range(stop) => 0 to stop-1  with a step 1, start = 0 by default
		- If we don't give the start value -> it will by default considered as 0
		- If we don't give the step value -> it will by default considered as 1
			- So 
				- Start => 0
				- Step => 1
				- Stop => Stop - 1

```
  
######################################  
# Range - 3  
# range(stop) = > 0 to stop - 1 with a step 1, start = 0 by default  
# start = 0, step = 1 => 0,1,2,3,4  
for i in range(5):  
    print(i)

Output Response -
0
1
2
3
4
```


--------
--------

- Range Function Summary
	- range(start, stop, step)
		- stop index is not included
	- range(start, stop)
		- step = 1 by default
	- range(stop)
		- start = 0
		- step = 1
		- index => stop-1 [stop index is not included]

---
---

- We shall look at the use case specifically with the sequences on how we can use it.

1. we shall print the indexes of the list groceries
```
# we shall print the indexes of the list groceries  
groceries = ["salt","milk","sugar"]  
for index in range(len(groceries)):  
    print(index)

Output Response -
0
1
2
```

2. we shall print both indexes and values of the list
```
###########  
# profit of quarter 1 -  
# profit of quarter 2 -  
# profit of quarter 3 -  
# profit of quarter 4 -  
  
profits = [9, 11, 6, 10]  
for index in range(len(profits)):  
    quarter = index + 1  
	print(f"profit of quater {quarter} - {profits[index]}")
	
Output Response -
profit of quater 1 - 9
profit of quater 2 - 11
profit of quater 3 - 6
profit of quater 4 - 10
```

---
---
