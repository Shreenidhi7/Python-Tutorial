
- In the previous section we looked at the syntax of user defined function
- This lecture, we will look at some examples on how to create our own functions
- Below is the function which is created
	- What happens when we run the file?
```
# declaring/defining a function
def greeting_someone():  
    print("Hello, Good Morning!")  
    print("Its a beautiful day!")
    
Output Response -

```

- There is nothing in the output.
	- We have some code, but we donot see the output
	- This is because, we have defined the function but we haven't called the function.
- To call a function, what do we have to do?
	- we need to write the function name
```
# declaring/defining a function  
def greeting_someone():  
    print("Hello, Good Morning!")  
    print("Its a beautiful day!")  
  
# calling a function  
greeting_someone()

Output Response -
Hello, Good Morning!
Its a beautiful day!
```

- When we define a function and doesn't call it, then that particular function will not be executed.
- When we call the function, the control goes to the line of code where the function is declared and the block of lines inside the function will get executed.

- If we want to use/call this function multiple times, it can be done by calling the function again and again
	- greeting_someone()
	- greeting_someone()
	- greeting_someone()

----

- We can enhance this function by using some arguments in this.
	- Argument is something which we pass to the function and that value gets inside the function
	- If we want a specific message to the declared in the function, then arguements will be very helpful
```
# declaring/defining a function  
def greeting_someone(name):  
    print(f"Hello, {name} Good Morning!")  
    print("Its a beautiful day!")  
  
# calling a function  
greeting_someone("Mark")  
greeting_someone("Carol")  
greeting_someone("John")

Output Response -
Hello, Mark Good Morning!
Its a beautiful day!
Hello, Carol Good Morning!
Its a beautiful day!
Hello, John Good Morning!
Its a beautiful day!
```

- In the above example, we have just taken 1 argument, but we have have as many as arguments we need and we have to use that variable inside our program.
	- It can be multiple values that we can pass.

---

- Lets try to write a function to check if a particular value is odd or even.

```
# defining a function  
def evenOrOdd(number):  
    if number % 2 == 0:  
        print("Even")  
    else:  
        print("Odd")  
  
# calling a function  
evenOrOdd(10)  
evenOrOdd(11)  
evenOrOdd(99)  
evenOrOdd(100)

Output Response -
Even
Odd
Odd
Even
```

- In the above program, we have written the even/odd logic once inside the function and we are calling it 4 times
	- So we don't have to write the login again and again
- This is what re-useability of code can be done using functions
- This is the main reason we write functions
- The other reason we write functions is that the code is clean
	- We write it once in a block - it looks cleaner/its more visible
	- The code becomes readable/reusable

----

- Multiple Arguments
	- 1st value goes to the 1st argument
	- 2nd value goes to the 2nd argument

```
def add(num1, num2):  
    result = num1 + num2  
    print(f"Result => {result}")  
  
add(1, 2)  
add(9, -4)
```

---
---
