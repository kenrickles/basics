# Project 3: Guess the Word

#### Due: Thursday 3 September

This is a game where the player must guess a secret word.

Begin the app by **forking** this repo: [https://github.com/rocketacademy/swe101-guess-the-word](https://github.com/rocketacademy/swe101-guess-the-word)



For each wrong guess the program adds to the figure: \(凸ಠ益ಠ\)凸

The player can only guess wrong 7 times before the game ends. \(the number of characters in the figure\)

Before you start read through the advice on how to start and the more comfortable sections to see what the basic and advanced versions of the game include. 

### How to Start

The first version of this game you can have a single, hard-coded secret word- `cat`.

The data structure you need to represent the game that guesses each individual letter in a word is an array of individual letters.

This will allow you to guess letters and find each letter guessed and the position of those letters in the word.

A word array would look like this: `var word = ['c','a','t'];`.

#### Game Play

When the user guesses a letter, you have to have the program look through the word array and determine if the user guessed correctly.

> "Looking through" means looping over the word array and comparing it to the letter the user has inputted.

When the user guesses there are two possibilities:

1. The user guesses incorrectly. Add a character to the figure that marks when they lose the game.
2. The user guesses correctly, add the letter to the word they are trying to complete.

\(In the first version you can just do basic output like how many guesses the user has left, and how many letters they have correct.\)

After checking the guess for the individual user guess, check for the state of the entire game:

If the user has guessed all the letters in the word, tell them they have won.

If the user has completed the figure tell them they lost.

### More Comfortable

#### Output Formatting

When the user types a correct guess show the correct guess in the location of the secret word. Show the number of letters in the secret word.

#### Easier / Harder Mode

Add different modes to the game. Change the secret word to a word with the same letter more than once.

The easy mode is when the word is like "guess" and the user guesses 's', then the game fills in both 's'. 

The hard mode is where the user has to guess each letter.

#### Name

Let the user enter their name at the beginning of the game.

#### More words

Add a list of words to the game. When it starts the game selects one random word.

#### Continue Play

When the user has played one game with one word, allow them to continue playing with another word. 
