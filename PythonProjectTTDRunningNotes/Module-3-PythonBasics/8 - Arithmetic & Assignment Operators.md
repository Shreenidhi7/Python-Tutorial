
**Operators in Python**
1. Lets consider the below lines of code
	1. x =10
	2. y = x +20
		1. x & y are variables
		2. 10 & 20 are literal values
		3. = & + are called operators
2. Operators are symbols to perform certain operations.
	1. These operations can have variable, values and operators in it.
		1. The varaibles & values are called "Operands"
3. An operation contain 2 things
	1. Operands
	2. Operators
4. Any Symbol [=,+ ,- ,% , / ] that performs any operation on operands are called Operators

```
x = 10
y = x + 20

# x,y - variables [operands]
# 10,20 - values [operands]
# =, + - operators  
```

5. There are different types of operators in python that are supported.
	1. Arithmetic Operators
	2. Assignment Operators


----

**Arithmetic Operator**
1. As the name suggests, the arithmetic operators are used to perfrom arithmetic operations.
	1. It means that it is used to perform basic mathematical operations like
		1. Addition [ + ]
		2. Subtraction [ - ]
		3. Multiplication [ * ]
		4. Division [ / ]
			1. Division Operator - Gives a Result/Output/Response in Floating Point
			2. The Division Operator gives you the "Quotient" as the output
			3. Ex: 10/5 - 2.0
			4. Ex: 10 / 3 = 3.33
			5. Even though the operands are int values, the output would be in Float
				1. [Single Division operator will give you output in Float]
		5. Floor Division [ // ]
			1. When Floor Division is performed, it wont do the fractional part.
			2. The Floor Division Operator gives you the "Quotient" as the output
				1. It only take the integer value [means the values after . is not performed/considered]
					1. [Double Division/Floor Division operator will give you output in Int]
			3. Ex: 10 // 3
				1. Output - 3
		6. Percent [Modulus] [ % ]
			1. It is also related to division
			2. The Modulus operator gives you the "Remainder" as the output
				1. It returns Integer value
			3. Ex: 10 % 3
				1. Output - 1
		7. Exponential Operator [Exponent] [ ** ]
			1. Its basically a (power of) the value
				1. Ex: 5 to the power of 2
					1. 5 * 5  = 25
				2. Ex: 3 to the power of 4
					1. Its 3 multiplied 4 times
					2. 3 * 3 * 3 * 3 = 81

```
# Operators
# Arithmetic Operators

num1 = 10
num2 = 5
num1
10
num2
5

----------
# + -> Addition
num1 + num2
15

----------
# - => Subtraction
num1 - num2
5

----------
# * => Multiplication
num1 * num2
50

----------
# / => Division [Single Division operator will give you output in Float]
num1 / num2
2.0

10 / 3
3.3333333333333335

----------
# // => Floor Division [Double Division operator will give you output in Int]
num1 // num2
2

10 // 3
3

----------
# % => Modulus
num1 % num2
0

10%3
1

----------
# ** => Exponential [Exponent] - Its basically a (power of) the value

5 ** 2
25

3 ** 4 [ 3 * 3 * 3 * 3 = 81 ]
81
```


---

**Assignment Operator**
1. As the name suggests, the Assignment operators are used to assign values to a variable.
	1. Ex: value = 100
		1. Equal To (=) is an assignment operator
	2. Ex: add = num1 + num 2
		1. Equal To (=) is an assignment operator
2. Assignment operators have something called "Compound Assignment Operators"
	1. Ex:
		1. x =10
		2. x
		3. 10
		4. x += 1  [# x = x+1]
	2. **x+=1** basically a shortcut of **x = x+1**
	3. How it operates?
		1. It does the operation and saves it back to same variable
	4. Compound Assignment Operator works with
		1. 1. Addition [ + ]
		2. Subtraction [ - ]
		3. Multiplication [ * ]
			1. Exponential Operator [Exponent] [ **  ]
		4. Division [ / ]
			1. Floor Division [ // ]
			2. Percent [Modulus] [ % ]


```
# Assignment Operators

value = 100

add = num1 + num2
add
15

# Compound Assignment Operator
x = 10
x
10

---
x += 1 #x = x+1
x
11

---
x -= 6 #x = x-6
x
5

---
x *= 10 #x = x*10
x
50

---
x /= 20 #x = x/20
x
2.5
```


---


