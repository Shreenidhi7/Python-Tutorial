
- In this section, we shall look at something called one line IF ELSE statements.
	- Its also called Ternary Operator
- If we remember the operator session, there were 3 types of operators depending on the operands.
	- Unary
	- Binary
	- Ternary

- What is one-line IF ELSE statements?
	- As the name suggests, in Python there is a concise way or concise syntax for writing simple IF-ELSE statements in single line.
	- This is also called Ternary operator.
	- This one-line or conditional expression basically evaluates the value based on the condition.
	- Syntax - true-expression if condition else false-expression

```
num = int(input("Enter a number: "))  
  
# normal way - traditional way  
# if num % 2 == 0:  
#     result = "Even"  
# else:  
#     result = "Odd"  
# print(result)  
  
# true-expression : if condition  
# false-expression : else condition  
# true-expression : if condition else false-expression  
print("Even") if num % 2 == 0 else print("Odd")

Output Response -
Enter a number: 1
Odd

Enter a number: 2
Even
```


---
---
