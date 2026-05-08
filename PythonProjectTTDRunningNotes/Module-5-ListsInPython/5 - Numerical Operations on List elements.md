
In this section, we shall look at the lists having numbers like integers or float
We shall look when the elements/items of the list are numbers, what operations could be performed on the list.

1. Finding the smallest/minimum number of the list
	1. Python provides the function called min()
2. Finding the biggest/largest/maximum number of the list
	1. Python provides the function called max()
3. Imagine that we have a string "Hi" in the list of numbers
	1. numbers = [10, 4, -1, 20, 5.5, 7, 1, "Hi"]
	2. What will happen here? Can we find the biggest/smallest number in this case where we have the other data type which is not a number(string) [That's not an integer/float]
		1. We will get the Type Error [ '<' not supported between instances of 'str' and 'int' ]
		2. When we do a min()/max() function, it internally does the comparison using the less than or greater than operator
		3. And it cannot compare an integer with string [it can compare the integer with float, but not with the string]
			1. Since the comparison is happening with comparison operator which is basically not supported between string and an integer and that's the reason its failing.
4. Finding the total of the numbers of the list
	1. Python provides the function called sum()

```
numbers = [10, 4, -1, 20, 5.5, 7, 1]  
  
# Smallest number in the list  
# min()  
print(numbers)  
print("Smallest numbers in the list =", min(numbers))  
  
# Largest/Biggest number in the list  
# max()  
print(numbers)  
print("Largest numbers in the list =", max(numbers))  
  
# Total of the numbers in the list  
# sum()  
print(numbers)  
print("Sum/Total of the numbers in the list =  ", sum(numbers))

Output Response - 
[10, 4, -1, 20, 5.5, 7, 1]
Smallest numbers in the list = -1
[10, 4, -1, 20, 5.5, 7, 1]
Largest numbers in the list = 20
[10, 4, -1, 20, 5.5, 7, 1]
Sum/Total of the numbers in the list =   46.5
```

----
----

