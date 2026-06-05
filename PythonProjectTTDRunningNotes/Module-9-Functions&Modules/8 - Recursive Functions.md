
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
- Without Recursion  

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

