# Guessing Game Flowchart

## Description

Heres how the game works:
- The computer picks a random number between 1 and 100.
- The player guesses a number.
- If the guess is not a number, it says its invalid and it will ask again.
- If the guess is too high or too low, it tells the player.
- If the guess is correct, it ends the game.

---
# Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> Generate["Generate random number (1-100)"]
    Generate --> Guess["Ask player for guess"]
    Guess --> CheckNumber{"Is input a number?"}
    CheckNumber -- No --> Error["Show 'Invalid input'"]
    Error --> Guess
    CheckNumber -- Yes --> Correct?{"Guess = Number?"}
    Correct? -- Yes --> Win["Show 'Correct!'"]
    Win --> End([End])
    Correct? -- No --> TooHigh?{"Guess > Number?"}
    TooHigh? -- Yes --> High["Show 'Too high'"]
    High --> Guess
    TooHigh? -- No --> Low["Show 'Too low'"]
    Low --> Guess

 %% Documentation:
    %% 1. Start - The game begins.
    %% 2. Generate - The computer picks a random number from 1 to 100.
    %% 3. Guess - The player inputs their guess.
    %% 4. CheckNumber - Validates if the input is a number.
    %% 5. If not a number, show error and ask again.
    %% 6. If a number, check if it matches the random number.
    %% 7. If correct, show success message and end the game.
    %% 8. If guess is too high, inform player and ask again.
    %% 9. If guess is too low, inform player and ask again.




