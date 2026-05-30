
- Till now we have learnt what are loops, types of loops [for loop and while loop] and few examples on that.
- In this lecture, we will bring all those concepts that we have learnt till now with loops and see some exercise.
- Problem
	- Write a program to simulate a roll of die/dice. A die has 6 faces with numbers 1 to 6 written on them. The program should randomly print a number between 1 and 6

```
"""  
Write a program to simulate a roll of die/dice.  
A die has 6 faces with numbers 1 to 6 written on them.  
The program should randomly print a number between 1 and 6  
"""  
  
import random  
print("Welcome to the game of rolling a dice")  
while True:  
    choice = input("Please 'Enter' to roll and dice or 'Q' to quit: ")  
    if choice == "Q":  
        print("Thank you for playing the game, bye!")  
        break  
    elif choice == "Enter":  
        number = random.randint(1,6)  
        print(f"Your number is {number}")  
    else:  
        print("Invalid input, please try again")
        
Output Response -
Welcome to the game of rolling a dice
Please 'Enter' to roll and dice or 'Q' to quit: Enter
Your number is 2
Please 'Enter' to roll and dice or 'Q' to quit: Enter
Your number is 4
Please 'Enter' to roll and dice or 'Q' to quit: Enter
Your number is 1
Please 'Enter' to roll and dice or 'Q' to quit: Enter
Your number is 5
Please 'Enter' to roll and dice or 'Q' to quit: qwerty
Invalid input, please try again
Please 'Enter' to roll and dice or 'Q' to quit: enter
Invalid input, please try again
Please 'Enter' to roll and dice or 'Q' to quit: q
Invalid input, please try again
Please 'Enter' to roll and dice or 'Q' to quit: Q
Thank you for playing the game, bye!
```

---
---

To handle the case where the user provides a space before or after providing the value to Enter or Q the game
- It can be done by using strip
	- Any trailing or leading space can be deleted.
		- choice = input("Please 'Enter' to roll and dice or 'Quit' to quit: ")  
		- choice = choice.strip()  

```
"""  
Write a program to simulate a roll of die/dice.  
A die has 6 faces with numbers 1 to 6 written on them.  
The program should randomly print a number between 1 and 6  
"""  
  
import random  
print("Welcome to the game of rolling a dice")  
while True:  
    choice = input("Please 'Enter' to roll and dice or 'Quit' to quit: ")  
    choice = choice.strip()  
    if choice == "Quit":  
        print("Thank you for playing the game, bye!")  
        break  
    elif choice == "Enter":  
        number = random.randint(1,6)  
        print(f"Your number is {number}")  
    else:  
        print("Invalid input, please try again")
```


---
---
