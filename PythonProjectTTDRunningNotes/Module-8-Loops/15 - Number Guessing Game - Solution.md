
```
import random  
num = 1  
print("Welcome to the Number Guessing Game. We have a number to be guessed. You have 10 attempts")  
print("The secret number is between 1 and 50")  
secretNumber = random.randint(1, 50)  
attempts = 10  
is_guess_correct = False  
  
while num<=10:  
    print(f"You have {attempts} attempts left")  
    userGuess = int(input("Enter your guess: "))  
    if userGuess==secretNumber:  
        print("Congratulations! Your guess is correct!")  
        is_guess_correct = True  
        break    else:  
        if userGuess < secretNumber:  
            higher_or_lower = "higher"  
        else:  
            higher_or_lower = "lower"  
        print(f"Your guess is wrong! Try {higher_or_lower} number")  
    num = num + 1  
    attempts -= 1  
  
if not is_guess_correct:  
    print("Bad Luck!! You have exhausted all your attempts and couldn't guess the number.")  
print(f"The secret number was {secretNumber}. Game Over!")
```

