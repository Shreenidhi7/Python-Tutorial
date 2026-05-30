
- This section, we will basically use the concept that we have learned about loops and conditional statements to create a small game.

- Problem Statement
	- Create a simple number guessing game
	- The user gets 10 chances to guess a number.
	- If the user guesses the number before 10 chances, stop asking the number from the user.
		- Say congrats and end the game.
	- If the user never guesses the number, ask them 10 times and then end the game!!

```
"""  
- Problem Statement  
    - Create a simple number guessing game    - The user gets 10 chances to guess a number.    - If the user guesses the number before 10 chances, stop asking the number from the user.       - Say congrats and end the game.    - If the user never guesses the number, ask them 10 times and then end the game!!"""  
  
import random  
randomNumber = random.randint(10, 50)  
numberOfGuesses = 0  
print("Welcome to the Number Guessing Game. We have a number that needs to be guessed. You have 10 chances to guess the number.")  
print("The random/secret number is between 10 and 50")  
print("You have 10 attempts to guess the number.")  

# while True:  
#     users_guess =  int(input(f"Guess the number between 1 and 10 - Your Guess Attempt is {numberOfGuesses+1} - "))  
#     if users_guess == randomNumber:  
#         print("Congratulations! You guess is correct!")  
#         print(f"The number was {randomNumber}. Game Over!")  
#         break  
#     else:  
#         numberOfGuesses = numberOfGuesses + 1  
#         if numberOfGuesses == 10:  
#             print("You have taken 10 chances to guess the number! Better Luck Next time!")  
#             print("The Number to be guessed was: ", randomNumber)  
#             break  
# print("Ending the game")  
  
  
while True:  
    users_guess =  int(input(f"Guess the number between 10 and 50 - Your Guess Attempt is {numberOfGuesses+1} - "))  
    if users_guess > randomNumber:  
        numberOfGuesses = numberOfGuesses + 1  
        print("Your guess is wrong! try lower number")  
        print(f"You have {10 - numberOfGuesses} attempts to guess the number.")  
        if numberOfGuesses == 10:  
            print("You have taken 10 chances to guess the number! Better Luck Next time!")  
            print("The Number to be guessed was: ", randomNumber)  
            break  
    elif users_guess < randomNumber:  
        numberOfGuesses = numberOfGuesses + 1  
        print("Your guess is wrong! try higher number")  
        print(f"You have {10 - numberOfGuesses} attempts to guess the number.")  
        if numberOfGuesses == 10:  
            print("You have taken 10 chances to guess the number! Better Luck Next time!")  
            print("The Number to be guessed was: ", randomNumber)  
            break  
    else:  
        print("Congratulations! You guess is correct!")  
        print(f"The number was {randomNumber}. Game Over!")  
        break  
print("Ending the game")
```