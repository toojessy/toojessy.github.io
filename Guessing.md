# Task
    - Your task is to create a detailed flowchart that describes this guessing game. 
    - You will use Mermaid syntax to illustrate this flowchart in a GitHub markdown (.md) file. 
    - Your flowchart should comprehensively cover all logical components of the game that need to be tested.

''' mermaid
flowchart TD
    Start([Start]) --> End([End])
    Start([Start]) --> GenerateNumber[Generate Random Number]
    GenerateNumber --> AskUser[Ask User for a Guess]
    AskUser --> InputValidation{Is Input Valid?}
    InputValidation -- Yes --> CheckGuess[Check Guess]
    InputValidation -- No --> InvalidInput[Display "Invalid Input"]
    InvalidInput --> AskUser
    CheckGuess -->|Correct| CorrectGuess[Display "Correct! You guessed it!"]
    CheckGuess -->|Too High| TooHigh[Display "Too High! Try again."]
    CheckGuess -->|Too Low| TooLow[Display "Too Low! Try again."]
    TooHigh --> AskUser
    TooLow --> AskUser
    CorrectGuess --> End([End])
'''
### Start: The game begins, initializing necessary variables.
### Generate Random Number: The program randomly selects a number within a specified range (e.g., 1 to 100).
### Ask User for a Guess: The user is prompted to input their guess for the generated number.
### Input Validation: The program checks if the user input is valid:
### Yes: If the input is valid (e.g., numeric and within range), the program proceeds to check the guess.
### No: If the input is invalid (e.g., non-numeric or out of range), the program displays "Invalid Input" and prompts the user to guess again.
### Check Guess: The program compares the user’s guess to the randomly generated number:
### Correct: If the guess matches the number, the program displays "Correct! You guessed it!" and ends the game.
### Too High: If the guess is higher than the number, the program displays "Too High! Try again." and prompts for another guess.
### Too Low: If the guess is lower than the number, the program displays "Too Low! Try again." and prompts for another guess.
### End: The game concludes, potentially allowing the user to play again or exit.
