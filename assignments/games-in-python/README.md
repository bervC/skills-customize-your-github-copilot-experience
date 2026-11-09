# 📘 Assignment: Hangman Game

## 🎯 Objective

Build a Hangman game that practices Python strings, loops, conditionals, random selection, and user input.

## 📝 Tasks

### 🛠️ Set Up the Game

#### Description
Choose a secret word at random and prepare the variables needed to track the player's progress.

#### Requirements
Completed program should:

- Select one word at random from the provided `words` list.
- Track the letters the player has guessed and the number of incorrect guesses.
- Set a maximum of six incorrect guesses.

### 🛠️ Accept and Track Guesses

#### Description
Ask the player to guess letters and update the displayed word and remaining attempts after each guess.

#### Requirements
Completed program should:

- Prompt the player for one letter at a time.
- Show correctly guessed letters in their matching positions and underscores for letters not yet guessed (for example, `_ _ _ _ _ _`).
- Record incorrect guesses and show how many attempts remain.
- Avoid counting a letter more than once if it has already been guessed.

### 🛠️ End the Game

#### Description
Continue the game until the player guesses the word or runs out of incorrect guesses, then show the outcome.

#### Requirements
Completed program should:

- Stop when all letters in the secret word have been guessed or the player has made six incorrect guesses.
- Display a win message when the player guesses the word.
- Display a lose message and reveal the secret word when the player runs out of attempts.
