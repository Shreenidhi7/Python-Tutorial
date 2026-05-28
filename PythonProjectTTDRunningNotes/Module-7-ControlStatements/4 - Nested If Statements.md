
- Till now we have seen IF, ELSE, ELIF conditional statements
- This section we shall discuss about NESTED IF
- NESTING means something inside someting
	- IF inside IF

```
"""  
if marks >= 60, student is pass else student is fail  
and if student is pass, then we print the grade  
marks >= 90 : Grade A  
marks 80 and 89 : Grade B  
marks 70 and 79 : Grade C  
marks 60 and 69 : Grade D  
"""  
  
#nested-if  
marks = float(input("Enter your marks: "))  
if marks >= 60:  
    print("Congrats, You have passed the exam!")  
    if marks >= 90:  
        print("Grade A")  
    elif 80 <= marks < 90:  
        print("Grade B")  
    elif 70 <= marks < 80:  
        print("Grade C")  
    else:  
        print("Grade D")  
else:  
    print("You have failed the exam!")
    
    
Output Response -
Enter your marks: 55
You have failed the exam!

Enter your marks: 65
Congrats, You have passed the exam!
Grade D

Enter your marks: 75
Congrats, You have passed the exam!
Grade C

Enter your marks: 85
Congrats, You have passed the exam!
Grade B

Enter your marks: 95
Congrats, You have passed the exam!
Grade A

```


---
---
