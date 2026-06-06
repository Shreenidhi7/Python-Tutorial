
- This section, we will look what is recursion and how to create a recursive function in python
	- Recursion is a process in which a function calls itself till a certain condition is not met.
	- In simple words, a function that calls itself is a recursive function.
	- The process of writing a function and the function calling itself until a certain condition is met is called recursion
	- To understand this, we shall take an example of factorial
		- Factorial is a mathematical calculation that is performed.
			- n => n * (n-1) * (n-2) * .....
				- n!
			- 4! = 4 * 3 * 2 * 1
				- 24

- Before we understand how to use recursive function for the above example, lets try to create a normal function using for loop or while loop and see how it can work and then we will learn how to write the same thing using recursion and recursive function.

- Here for the factorial example, we have to keep on multiplying the numbers by reducing it.

###### - Without Recursion  

```
"""  
Recursion is a process in which a function calls itself till a certain condition is met  
Factorial of n => n * (n-1) * (n-2) ....  
representation of factorial => n!  
4! = 4 * 3 * 2 * 1 = 24  
"""  
  
###############  
# Without Recursion  
  
def fact(num):  
    factorial = 1                           # num=5, fact=1  
    while num >= 1:                         # num=5, 5>=1                   #num=4, 4>=1            #num=3,3>=1                 #num=2,2>=1                 #num=1, 1>=1                #num=0, 0 !>= 1  
        factorial = factorial * num         # factorial = 1*5 => 5          #5*4 => factorial=20    #20*3 => factorial=60       #60*2 => factorial=120      #120*1 => factorial=120  
        num = num - 1                       # num=num-1, 5-1=> 4, num=4     #4-1=3, num=3           #3-1=2, num=2               #2-1=1, num=1               #1-1=0, num=0  
    return factorial                        # factorial=120  
  
num = 5  
print(f"Factorial of {num} is {fact(num)}")

Output Response -
Factorial of 5 is 120
```

---

###### - With Recursion
- With Recursion we have to understand one thing is that there are 2 conditions/2 parts for recursive function.
	- Base/Terminal Condition
		- Stop Calling Itself
			- The base condition decides when the function (the recursive function) should stop calling itself.
				- If not, then it will keep on calling infinitely, we have stop somewhere.
	- Recursive Condition
		- When a function calls itself, how it should call.

- Example- 
	- In case of factorial
	- n! => n * (n-1) * (n-2) * ..... * 1
	- n! => n * (n-1)!
	- n! => n * (n-1) * (n-2)! .....
		- 1st write the base condition.  
		- Next we write the logic on how function should call itself.

```
##################  
# With Recursion  
'''  
There are 2 parts of the recursive function  
1. Base/Terminal Condition  
    - Deciding when the function should stop calling itself2. Recursive Condition  
    - How to function should call itself.'''  
  
"""  
Factorial Example:  
n! = n * (n-1) * (n-2) .... * 1  
n! = n * (n-1)!  
n! = n * (n-1) * (n-2)! ........  
"""  
  
"""  
2. 1st write the base condition.  
3. Next we write the logic on how function should call itself. """  
  
def fact_rec(number):  
    if number == 1:  
        return 1  
    else:  
        factorial = number * fact_rec(number - 1)  
        return factorial  
fact_number_rec = fact_rec(4)  
print(fact_number_rec)

Output Response -
24
```

- when we call fact_rec(4), it sees number=4
	- 4 == 1 is a false, 
	- then if will not go inside the if condition, so it goes to else condition
	- in else, what we are doing is number * fact_rec(number-1)
		- 4 * fact_rec(3)
		- so when we do fact_rec(3), it calls the same function again
		- it means fact_rec(4) is calling fact_rec(3) [fact_rec itself is calling its own function]
			- here it will check 3 === 1 is a false
			- then it will not go inside the if condition, so it goes to else condition
			- in else, what are doing is number * fact_rec(number-1)
				- 3 * fact_rec(2)
				- so when we do fact_rec(2), it calls the same function again
				- it means fact_rec(3) is calling fact_rec(2) [fact_rec itself is calling its own function]
					- here it will check 2 === 1 is a false
					- then it will not go inside the if condition, so it goes to else condition
					- in else, what we are doing is a number * fact_rec(number-1)
						- 2 * fact_rec(1)
						- so when we do fact_rec(2), it calls the same function again
						- it means fact_rec(2) is calling fact_rec(1) [fact_rec itself is calling its own function]
							- here is will check 1 === 1 - its a True
							- then it will go inside the if condition and return 1
- fact_rec(4)
	- 4 * fact_rec(3)
		- 3 * fact_rec(2)
			- 2 * fact_rec(1)
				- 1
- 4 
	- 4 * 6 => 24 [final response]
		- 3 * 2 => 6
			- 2 * 1 => 2
				- 1 => 1

- It will keep on returning the value until it reaches the fact_rec(4)
- fact_rec(4) is 4 * 3 * 2 * 1 => 24
- Important - None of these calculation happens untill all the functions are called and we reach the base condition
	- The calculation will only start when the base condition is reached [ untill that it will keep calling the recursive function ( the functions recursively one by one ) ]
	- And soon as it reaches the base condition, in the reverse order it starts the calculation
- It has an advantage in which the code will become a little cleaner
- A huge task/or composite task can be broken down into simpler code.
- We can have the base condition and the function call itself again and again and when the base condition is reached it starts calculating in reverse order to reach our first call and give us the output of it.
- It might have some dis-advantages, if its a huge calculation and recursive function has to be called many number of times, it can be extensive and can take lot of memory [it can be a memory extensive task]
- Recursion can be useful when we want to break down a complex task into smaller chunks [ like write the login once and keep on calling it again and again untill the base condition is reached and the calculation is only done when the base condition is reached and it does the calculation is reverse order untill it reaches the 1st call]

---
---
