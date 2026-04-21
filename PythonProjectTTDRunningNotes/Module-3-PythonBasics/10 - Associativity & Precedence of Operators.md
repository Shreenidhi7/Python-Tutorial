
**Precedence in Python**
1. In simple words, it means the priority in which operations are performed in Python.
2. Example - Lets have a calculation wherein it involves multiple operators
	1. 5 + 10 * 6  = 65
		1. According to mathematics, multiplication will happen 1st and then the output of this(10*6) will be added to 5
3. If there are multiple operators in the calculation - **Precedence determines the order in which they are evaluated or its like which operation will get the priority to execute 1st**
4. In mathematics - Its called BODMAS
5. Lets take up logical operators and try to understand the precedence in it.
6. Example -
	1. name = "Shree"
	2. age = 29
	3. Lets have a complex conditional statements combining a couple of conditional operators
		1. name == "Shree" or name == "Nidhi" and age < 18
		2. My Guess = False
			1. name == "Shree" or name == "Nidhi" - it returns True
			2. age < 18 - it returns False
			3. so, True and False = False
	4. But the real answer would be "True". How?
		1. Lets find out here - **AND** gets executed 1st and **OR** will get executed next.
		2. name == "Nidhi" and age < 18 -> this gets executed 1st
			1. False and False -> False
		3. name == "Shree" or false
			1. True or False -> True
7. These results are because of **Operator Precedence**
8. **Thumb Rule - AND will get executed 1st and OR will follow.**
9. In arithmetic operation, we know the priority using the BODMAS.
	1. With other operators other than arithmetic operator -> Precedence concept comes into picture.
10. AND has the higher priority than OR

How to know which operation has the highest priority?
https://www.geeksforgeeks.org/python/precedence-and-associativity-of-operators-in-python/

**Question**
- What if we want to check the names first and then the age?
	- name = "Shree"
	- age = 29
		- name == "Shree" or name == "Nidhi" 

**Answer/Solution**
* The 1st priority is given to the brackets [()] as per the document
	* We can put brackets around the name values
		* (name == "Shree" or name == "Nidhi") and age < 18 
	* In this case, brackets will make sure that the **OR** operation happens 1st.
	* (name == "Shree" or name == "Nidhi") and age < 18
		*  True and False => False
* Similarly, in the arithmetic operation - if we need to perform + operation 1st -> we need to enclose  5 + 10 inside the brackets
	* Example -> 5 + 10 * 6
		* Actual Output - 65
	* Example -> (5+ 10) * 6
		* Actual Output - 90

**Few more Arithmetic Example:**
1.  100 / 10 * 10
	1. If we apply math[BODMAS] on this, then this would be 100/10 = 10
	2. Then 10 * 10 = 100.0 {It returns float}
	3. Even though division and multiplication have same precedence, why did it consider the division first?
		1. **Reason -> Its Left to Right precedence**
		2. **Concept -> *, @, /, //, % : Multiplication, matrix multiplication, division, floor division, remainder -> Associativity: Left to right****
	4. Lets take below example to understand this.
		1. 2 to the power of 1 and 1 to the power of 3
		2. 2 ** 1 ** 3
			1. Output - 8 [2*1 = 2 and 2*2*2 = 8] - Its Incorrect
			2. Actual Output - 2 [ 1*1*1 =1 and 2*1] - Its the correct answer - Here comes the concept of Associativity (Left to Right)
			3. **Reason -> Its Right to Left precedence**
		3. **Concept -> ** : Exponentiation -> Associativity: Right to left****

With the above example, [Left to Right/Right to Left precedence], we can explore the concept of Associativity

```
# Precendence

5 + 10 * 6
65

name = "Shree"
age = 29

name == "Shree" or name == "Nidhi" and age < 18
True

(name == "Shree" or name == "Nidhi") and age < 18
False

(5 + 10) * 6
90

100 / 10 * 10
100.0

2 ** 1 ** 3
2
```

----

**Associativity**
1. If and when we have 2 or more operations[2 or more operators], having the same expression [ means multiplication/division/floor division etx] and having the same precedence [means order/priority], we cannot decide which operation will happen first, but there is **a concept called Associativity in Python that will decide which operation will happen first.**
	1. Whether it will be in the order of  Left to Right or the other way.
2. If the precedence of 2 operators/ 2 or more operators are same, the associativity (Left to Right or Right to Left) will device which operation has to happen first.

**Question**
- How do we know what is the associativity of the operator
**Answer**
- Every operator having the same/similar precedence has the associativity defined.
	1. https://www.geeksforgeeks.org/python/precedence-and-associativity-of-operators-in-python/
	2. Example - 
		1. If we look at division and multiplication
		2. 100 / 10 * 10
			1. 100.0
		3. ==>  *, @, /, //, % : Multiplication, matrix multiplication, division, floor division, remainder -> ****Associativity:**** Left to right
			1. Associativity is "Left to Right"
				1. It means it will perform the division operation first and then the multiplication operation will happen next


---

Until now we saw arithmetic & assignment operators, comparison & logical operators
The classification that we have seen is that we have seen till now is depending on the operation that it performs.

1. Arithmetic operator are called arithmetic operators because they perform arithmetic operations
2. Assignment operators are called assignment operators because they are used to assign a value to a variable.
3. Logical operators are called logical operators because they are used to perform logical operations
4. Comparison operators compares the two operands.

Similarly we have classification of operators based on the **number of operands**
1. **Unary Operator**
	1. If an operator operates on only one operand, then its called Unary Operator.
		1. MINUS ( - )
			1. Example : Minus (-)
				1. -10
			2. We can ask a question on asking is it really an operation?
				1. Answer is Yes, because 10 is a positive number
					1. When we put/apply minus(-) in front of it, it is converted into negative number.
		2. NOT ( not )
			1. Example (not)
				1. not True
					1. False

2. **Binary Operator**
	1. Binary operators are operators that operates on 2 operands
	2. Most of the operators are binary.
		1. Example - [ +, -, *, / ]
	3. Minus ( - ) is actually one of the operator which are both "Unary" and "Binary" because we can perform 10 - 5 and also -10
		1. 10 - 5 => Its binary operator because it has 2 operands in it.
		2. -10 => Its unary operator because it has only one operand in it.

3. **Ternary Operator**
	1. Ternary operator by definition it means the operator that operates on 3 operands.
		1. It involves the concepts like if else (conditional statements) in python


---
