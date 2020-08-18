---
layout: post
title: Hangman
permalink: /projects/hangman/
---

# Introduction

Hangman is a popular word game. Person 1 chooses a word at his will and the goal of Person 2 is to predict the word by predicting one character at a time. At every step, Person 1 gives the following feedback to Person 2 depending on the predicted character:
1. If the character is present, Person 1 informs Person 2 of all the positions at which the character is present.
e.g. if the word is 'hello' and Person 2 predicts 'l', Person 1 has to report that the character 'l' is present at position 3 and 4.
2. If the character is not present, Person 1 simply reports that the character is not present in his/her word.

Refer to [this](https://en.wikipedia.org/wiki/Hangman_(game)) Wikipedia article for more details.

# Model

1. The main model consists of a RNN which acts as an encoder. It takes the encoded version of the incomplete string and returns the hidden state at the last time step of the last layer.
2. On the other hand, we take the missed characters, encode it into a vector and pass it through a linear layer.
3. The outputs from 1 and 2 are concatenated and we pass this concatenated vector through a hidden layer and map it to a final layer with number of neurons = size of vocabulary (26 in our case for the English alphabet).

The model is trained using Binary Cross Entropy Loss since it is a multi-label classification problem.
A pretrained model can be found [here](https://drive.google.com/open?id=1hVBlS3zxTqcVktVZEHTv2ivg-oKpr-KQ).
It is a 2-layer, 512 hidden unit GRU with dropout and trained using Adam.

# Playing the Game

You can try out the game by running *game.py*. It has a terminal-based interface.

You can find the code on [GitHub](https://github.com/methi1999/hangman).