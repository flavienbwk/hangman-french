# Hangman French to learn English

This hangman game was made for french people so they can learn english vocabulary in a funny way.

Hangman is an old word game that children played together on paper to test their vocabulary skills. This is the classic paper hangman word gam updated for the internet age.

You will be playing against a computer which selects a word from a list of categories. You must guess the letters in the words before you are hung. Wrong guesses add elements to the gallow that is gradually built at the bottom of the page.

## Rules

You have 10 attempts to select an existing letter in the word to guess. This word will be blank, with `_` to represent a letter, so you can know how much letters are in the word.

If you select a letter present in the word to guess, it will displays.  
You have to find all the leters present in this word to win.

## How to play ?

Just click on `index.html`, it will launch your internet browser.  
Then, you just have to play !

## How to add more words ?

All is in `script.js`, see the `dictionary` variable :
```
var dictionary = {
    categories: [
      {
        category: "Health",
        words: [
          {
            word: "skin",
            hint: "peau"
          },
          [...]
```

Just add the words and categories you want as structured in the initial variable.

## How it was built ?

The initial requirement was to build a simple game for people to learn english. So it had to compatible with most of people's devices.  
An in-browser game was obvious.

The first part consisted in finding a structure to reference a dictionary of words, along with their categories and hints.

Second was about finding an interface for people to enter the letters.  
A simple input was not satisfying, because I wouldn't be able to gray out some letters so people can easily know what letter they already put.  
The best solution was to represent the alphabet letters.

Third, and the most tricky, was to create the gallow. It was about canvas pixels to draw depending on the attempts left.