
- In this section, we shall discuss on the basic operations on the sets

Membership Operators [ in and not in ]
- The "in" operator checks and gives us True if any element/item "present" in the List/Tuple and in Sets
- The "not in" operator checks and gives us False if any element/item "not present" in the List/Tuple and in Sets

```
nums = {1, 3, 2 , 0, -1}  
  
# membership operator - in and not in  
print(f"membership operators - in and not in")  

print(0 in nums)  
print(10 not in nums)  
  
print(5 in nums)  
print(1 not in nums)

Output Response -
membership operators - in and not in
True
True
False
False
```

----

- We already know that we cannot do indexing and slicing on sets. So what else can we do in sets?
	- Can we perform concatenation on sets?
- No, we cannot perform concatenation operation on sets
```
# concatenation operation - not possible on sets  
print(f"Concatnation Operation on Sets - Not Possible")  
num1 = {1, 2, 3}  
num2 = {4, 5, 6}  
print(num1 + num2)

Output Response -
Concatnation Operation on Sets - Not Possible
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\5-BasicOperationsOnSets.py", line 16, in <module>
    print(num1 + num2)
          ~~~~~^~~~~~
TypeError: unsupported operand type(s) for +: 'set' and 'set'
```


Repeating Sets?
- Not Supported
- Repetition could be done on Lists/Tuples & Strings but not in Sets
```
# repetition operation - not possible on sets  
print(f"Repetition Operation on Sets - Not Possible")  
print(num1 * 3)

Output Response -
Repetition Operation on Sets - Not Possible
Traceback (most recent call last):
  File "D:\Python\PythonTTDTutorial\Tuples, Sets & Dictionaries\5-BasicOperationsOnSets.py", line 20, in <module>
    print(num1 * 3)
          ~~~~~^~~
TypeError: unsupported operand type(s) for *: 'set' and 'int'
```

---

- Sets are similar to the Mathematical Sets
- Mathematics has some set theory
	- Union of Sets
	- Intersection of Sets
	- Difference b/w Sets etc
- Python Sets and Mathematical Sets are similar to each other.
- Python supports the Mathematical Set Operation on the Set data-type