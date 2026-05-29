
- In last section, we looked at what is while loop, how it is different from for loop and basic example of while loop.
	- While loop is not just used for generating numbers
	- It is used for more than that.
- If the condition never becomes FALSE, the while loop will be continuously run and that's called an Infinite loop.
	- Example -
		- while True:
			- print("Hello")
	- The while condition will never becomes False here, it will keep on printing Hello.....
	- This is called an Infinite loop.
	- But these conditions can be useful in many cases.
		- Lets say we want to run something continuously and the condition is something which we don't want to rely.
		- But internally we do something and when the condition is met, we basically break from the loop. [We know that we have BREAK statement, that makes us come out of the loop]
	- So, we can run the while loop infinitely and keep on printing something or doing something and if some condition is met, we come out of the loop

```
correct_password = "Python"  
  
while True: #infinite loop  
    user_password = input("Enter your password: ")  
    if user_password == correct_password:  
        print("Password is Correct! Congrats.")  
        break  
    else:  
        print("Password is not Correct! Try Again.")  
print("Logged in")

Output Response -
Enter your password: Java
Password is not Correct! Try Again.
Enter your password: python
Password is not Correct! Try Again.
Enter your password: javascript
Password is not Correct! Try Again.
Enter your password: Python
Password is Correct! Congrats.
Logged in
```

---
---

```
num = 20  
  
while num >= 10:  
    print(num)  
    num = num - 2
    
Output Response -
20
18
16
14
12
10
```

---
---
