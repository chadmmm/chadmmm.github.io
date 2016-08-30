---
published: false
layout: project
type: project
image: images/Chalkboard.png
title: Tic Tac Toe
permalink: projects/TicTacToe
date: 2016
labels:
  - Java
  - EZ graphics
summary: A game of Tic Tac Toe with a simple computer player feature.
---

<img class="ui large rounded image" src="../images/Chalkboard.png">

<H2>Summary</H2>
This Tic Tac Toe game was my final project for my Introduction to Computer Science I class. This project holds significance to me, because at the beginning of the semester, I had no programming experience and by the end of the semester, I was able to create a project with a group of my own choice. The project only required that we used the different skills that we learned in the class. Because the requirements were so open, I felt that this project was more of a project instead of an assignment. My group of 3 people was able to finish the project with a lot of time to spare, but all of us wanted to keep on working on it until the deadline to improve more on it.

<H2>Features/How to Play</H2>
  All of the graphics in this game were created using the EZ Graphics media library. When the game is first started there is a start screen that gives the 

<H2>How it was made</H2>
This Minesweeper game makes use of the array list and stack data structures. The array list data structure is used to store the high scores. The high scores are then sorted in the array list using insertion sort. The stack data strucutre is used in the algorithm used to clear the board spaces after a click. 

I was responsible for the win/lose, reset game, and high scores feature in this project. The win function determines whether the game is in progress, won, or lost. Once the game state is set by the win function, a dialog box is triggered to pop up to notify the player that they won the game. The reset game function clears all of the elements on the board and then randomly generates a new board. I ran into a few obstacles when working on this part because all of the elements were not clearing from the game board. The high scores features reads any saved scores from a text file and adds it to an array list. Once the game is finished, the score is added to the array list and then the array list is sorted using insertion sort. After the sorting is done, the scores and player names in the array list is then written to the saved high scores text file. Whenever a user views the high scores, the high scores are read from the saved text file. 
