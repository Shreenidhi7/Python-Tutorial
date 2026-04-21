
**Area of Triangle**

```
"""  
When all the length of the sides of the triangle is known - a, b, c  
Formula:  
Semi Perimeter (s) = (a + b + c)/2  
Area of Triangle = square root of (s * (s-a) * (s-b) * (s-c))  
"""  
  
a = float(input("Enter first side: "))  
b = float(input("Enter second side: "))  
c = float(input("Enter third side: "))  
s = (a + b + c) / 2  
print("The semi perimeter of the triangle is:", s)  
  
area = s * (s - a) * (s - b) * (s - c) ** 0.5  
print("The area of the triangle with given side is:", area)  
# round it off to 2 decimal points  
print("The area of the triangle with given side is:", round(area, 2))

Terminal ->
Enter first side: 7
Enter second side: 8
Enter third side: 9
The semi perimeter of the triangle is: 12.0
The area of the triangle with given side is: 415.6921938165305
The area of the triangle with given side is: 415.69
```


----

**Simple Interest**

```
"""  
Simple Interest = (P * T * R)/100  
P -> Principal Amount  
T -> Time Duration  
R -> Rate of Interest  
"""  
  
principal_amount = float(input("Enter the principal amount: "))  
time_duration = float(input("Enter the time duration: "))  
rate_of_interest = float(input("Enter the rate of interest: "))  
  
simple_interest = (principal_amount * time_duration * rate_of_interest)/100  
print("The simple interest calculation is ", simple_interest)

Terminal ->
Enter the principal amount: 10000
Enter the time duration: 12
Enter the rate of interest: 8
The simple interest calculation is  9600.0
```

----

**Compound Interest**

```
"""  
Compound Interest =  
P -> Principal Amount  
T -> Time Duration  
R -> Rate of Interest  
  
Amount = P [ 1 + R/100] ** T  
Compound Interest = A - P  
"""  
  
principal_amount = float(input("Enter the principal amount: "))  
time_duration = float(input("Enter the time duration: "))  
rate_of_interest = float(input("Enter the rate of interest: "))  
  
# Amount Calculation  
# amount1 = principal_amount * (1 + rate_of_interest / 100) ** time_duration  
amount2 = principal_amount * pow((1 + rate_of_interest / 100), time_duration)  
# print("The amount is:", amount1)  
  
print("Amount Calculation")  
print("The amount is:", amount2)  
print("The amount is rounded to 2 digits:", round(amount2, 2))  
  
# Compound Interest Calculation  
compoundInterest = amount2 - principal_amount  
compoundInterest_rounded = round(amount2, 2) - principal_amount  
print("Compound Interest Calculation")  
print("The compound interest is:", compoundInterest)  
print("The compound interest is:", compoundInterest_rounded)

Terminal ->
Enter the principal amount: 10000
Enter the time duration: 15
Enter the rate of interest: 3
Amount Calculation
The amount is: 15579.674166007651
The amount is rounded to 2 digits: 15579.67
Compound Interest Calculation
The compound interest is: 5579.674166007651
The compound interest is: 5579.67

```

----

Right Angled Triangle

```
"""  
Right Angled Triangle Calculation  
2 sides are already given, need to find out the 3 side  
Formula - 1/2 * b * h  
without the 3rd side we can still calculate the area of triangle = 1/2 * b * h  
"""  
  
base_of_triangle = float(input("Enter the base of triangle: "))  
height_of_triangle = float(input("Enter the height of triangle: "))  
  
area = 1/2 * base_of_triangle * height_of_triangle  
print("Area of Right Angled Triangle Calculation", area)

Terminal ->
Enter the base of triangle: 5
Enter the height of triangle: 6
Area of Right Angled Triangle Calculation
Area of Right Angled Triangle Calculation 15.0
```

---
