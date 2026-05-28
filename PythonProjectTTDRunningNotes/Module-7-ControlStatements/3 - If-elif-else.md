
- We shall continue conditional statements in this section as well.
- Till now we have seen IF and ELSE [ IF and IF-ELSE ]
- We have understood that we have one condition, if the condition is true, the execution goes to the if block and if the condition is false, the execution goes to the else block
- Now lets take an example wherein lets imagine that we have multiple conditions to be checked for a particular scenario.

```
"""  
marks >= 90 : Grade A  
marks 80 and 89 : Grade B  
marks 70 and 79 : Grade C  
marks 60 and 69 : Grade D  
marks < 60 : Grade F  
"""  
  
# if-elif-else  
marks = float(input("Enter marks: "))  
if marks >= 90:  
    print("Grade A")  
elif marks >= 80 and marks < 90:  
    print("Grade B")  
elif marks >= 70 and marks < 80:  
    print("Grade C")  
elif marks >= 60 and marks < 70:  
    print("Grade D")  
else:  
    print("Grade F")
    
Output Response -
Enter marks: 90
Grade A

Enter marks: 89
Grade B

Enter marks: 70
Grade C

Enter marks: 65
Grade D

Enter marks: 59
Grade F

```

---
---

In PyCharm editor, there is a wobbling line for all the statements
marks >= 80 and marks < 90
marks >= 70 and marks < 80
marks >= 60 and marks < 70
- This indicates a warning, when we hover on it, its asking us to simply chained comparison, so if we click on that, it will change the view of the conditional statement
80 <= marks < 90
70 <= marks < 80
60 <= marks < 70
- This is called Chained Expression. This is now the standard way of doing things.


---
---
