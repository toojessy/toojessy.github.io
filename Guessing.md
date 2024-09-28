## Task
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
