
- This section we will see about Anonymous function
	- Anonymous function is a function which doesn't contain any name.
	- It is also called as Lambda function

- Regular Function
```
# Regular Function  
def add1(n):  
    return n+1  
result = add1(1)  
print(result)

Output Response -
2
```

- Lambda Function
```
# LAMBDA Function  
'''  
Syntax - lambda argument : expression  
'''  
  
func = lambda n : n+1  
print(func(2))

Output Response -
3
```

---
---
- Regular Function
	- 2 Arguments
```
def add1(n, m=10):  
    print(n+1,m+1)  
    return n+1, m+1  
result1 = add1(1)  
result2 = add1(2,3)  
print(result1,result2)

Output Response -
2 11
3 4
(2, 11) (3, 4)
```

- Lambda Function
	- 2 Arguments
```
func = lambda x,y: x+y  
result = func(1, 2)  
print(result)

Output Response -
3
```

---
---
