
**Comparison Operators**
1. Comparison operators are the operators that are used to compare certain entities
	1. Mainly it will compare 2 operands/2 values
2. Comparison operators are
	1. Equal To ( == )
	2. Not Equal To ( != )
	3. Greater Than ( > )
	4. Lesser Than ( < )
	5. Greater Than or Equal To ( >= )
	6. Lesser Than or Equal To ( <= )
3. In general, comparison operator return either True or False


**Equal To/Double Equal/Equality Operator** [ == ]
1. If the left side value and the right side value are the same, then the Equality/Double Equal/Equal To operator will give us/return "True"
2. If the left side values doesn't match with the right side values, then the Equality/Double Equal/Equal To operator will give us/return "False"
3. Equality operator/comparison operator are not only used with numbers[Integers/Floats]
	1. But can be used with any kind of data type.
4. Python is a case sensitive language
	1. Comparison b/w "Python" & "python" returns "False"

```
# Comparison Operator
# ==, !=, >, <, >=, <=

# ==
num1 = 100
num2 = 90
num3 = 90

num1 == num2
False

num2 == num3
True

# String
"Python" == "python"
False

"python" == "python"
True
```

----

**Not Equals To [ != ]**
1. Not Equals To operator gives us/returns us "True", when both the left side operand and the right side operand are not same [ the values of both of them are different ]
2. Not Equals To operator gives us/return us "False", when both the left side operand and the right side operand are same [ the values of both of them are same ]

```
# !=
num1 != num2
True

num2 != num3
False
```

---

**Greater Than [ > ]**
1. Greater Than operator gives us/return us "True", if the left side operand value is greater than the right side operand value
	1. Example - num1 > num2
2. Greater Than operator gives us/return us "False", if the left side operand value is not greater than the right side operand value
	1. Example - num3 > num 1

```
# >
num1 > num2
True

num3 > num1
False

```


---

**Lesser Than [ < ]**
1. Lesser Than operator is the reverse of the Greater Than operator.
2. Lesser Than operator gives us/returns us "True", when the left side operand value is less than the right side operand value
	1. Example - num1 < num2

```
# <
num1
100
num2
90
num3
90

num1 < num2
False

num3 < num1
True
```

---

**Greater Than or Equal To [ >= ]**
1. In this case, we get a "True", if the left side operand value is either greater than or equal to the right side operand value.
	1. Example - num1 >= num2
2. If the left side value is less than the right side value, then it returns "False"

```
# >=
num1
100
num2
90
num3
90

num1 >= num2
True

num2 >= num3 [this case, num2 is not greater than num3, but are equal - so its a True]
True

num2 >= num1 [num2 is neither greater than/nor equal to num1 - so its a False]
False

```

---

**Lesser Than or Equal To [ <= ]**
1. It is similar to Greater Than Equal To but in an opposite way.
2. It will return "True", if the left side value is either less than or equal to the right side value.

```
# <=
num1
100
num2
90
num3
90

num2 <= num1
True

num2 <= num3
True

num1 <= num2
False

```

This basically concludes our comparison operators

---

**Logical Operators**
1. Logical operators as the name suggests, they look for logics.
	1. It means they actually work upon Boolean Values
		1. Boolean values are True & False
2. Logical Operator are
	1. AND
	2. OR
	3. NOT
3. Logical operators are used to basically combine conditional statements together, allowing us to perform operations based on multiple conditions.
	1. Example - 

**AND**
1. The 1st operand is "True" and the 2nd operand is "True", then the logic returned is "True"
	1. True and True
		1. True
2. If the 1st operand is "True" and the 2nd operand is "False", then the logic returned is "False"
	1. True and False
		1. False
3. If the 1st operand is "False" and the 2nd operand is "True", then the logic returned is "False"
	1. False and True
		1. False
4. If the 1st operand is "False" and the 2nd operand is "False", then the logic returned is "False"
	1. False and False
		1. False
Example - Shree, 29 years old
* I am Shree and I am 29 years old - True & True -> True
* I am Shree and I am 18 years old - True & False -> False
* I am Nidhi and I am 29 years old - False & True -> False
* I am Nidhi and I am 18 years old - False & False -> False

```
# Logical Operators => and, or, not

# and

True and True
True

True and False
False

False and True
False

False and False
False

```


---

**OR**
1. If one of the operand is "True", OR will return "True"

```
# or

True or True
True

True or False
True

False or True
True

False or False
False

```

---

**NOT**
1. NOT operator return "True", if the operand is "False" and vice versa.
2. NOT True -> False
3. NOT False -> True

```
# not

not True
False

not False
True

```

---

Example:

```
name = "Shree"
name
'Shree'
age = 29
age
29

name == "Shree" and age >=18
True
name == "Shree" and age == 30
False
name == "Shree" or age == 30
True
```


---
