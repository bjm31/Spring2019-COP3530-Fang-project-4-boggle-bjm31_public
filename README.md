# COP 3530 - Data Structures and Algorithms I

# Project 4 - Boggle

## Objective:

This project is meant to help you familiarize yourself with backtracking algorithms and the usage of hashing data structures. You will be recreating the game of 'Boggle', which is a game that involves identifying as many words as possible from a 4 x 4 grid of letter dice. Each dice has 6 letters on it. This game will be single player with the player seeking to identify all words in the grid. 

## Learning Outcomes:

Developer a program that uses:

- Multiple modules
- Arrays
- Sets
- Backtracking

## Preparation:

To complete this project, you need to make sure that you have read the following (notice that topics between projects build upon each other):

- Chapter 3 - Strings
- Chapter 4 - Array and Vector Basics
- Chapter 5 - Function Basics
- Chapter 7 - Objects and Classes Basics
- Chapter 9 - Modular Design and Makefiles
- Chapter 10 - Memory Management
- The Arrays Handout on Canvas
- Chapter 12 - Recursion
- Chapter 16 - Hashing
- Chapter 18 - Heaps and Backtracking (Primarily the Recursive examples)

## Problem Description:

Boggle is a popular word game by Hasbro for any number of players. However, in our version, we will be playing a single person version of the game. Boggle is played with a tray of 16 6-sided, letter dice, which is shaken to get 16 random letters arranged in a 4 x 4 grid. You will be generating this grid for the player. 

Players must find as many words as they can in the grid. The rules for the original game are as follows:

- The letters must be adjoining in a 'chain' with no wrapping. (Letter cubes in the chain may be adjacent horizontally, vertically, and diagonally.)
- Words must contain at least three letters.
- No letter cube may be used more than once within a single word.
- Words within other words are permissable (e.g., part and art).
- You will not receive more points for submitting the same word multiple times.

An example of a Boggle board is as follows:

B E N H
L A U M
I T L Z
R G A N

In the above board, there are several examples of words, including 'eat' (going straight down from e), 'bat' (going diagonal from b then straight down), and 'tan' (going up from t then diagonal to n). Proper names such as 'ben' do not count. 

You will also implement additional variant game modes on the original game as follows:

1. Try to determine the maximum score that can be achieved without repeating letters from previously selected words.
2. Allow for the player to wrap around the board horizontally and vertically.
3. Players get a random letter. This random letter can be inserted anywhere into any string of letters on the board. As an example, they may be be given the letter 't' and identify 'sar' on the board. They can use their extra letter to form the word 'star'. This can be done multiple times but only once per word. 

In order to have interesting games of Boggle, distribution of letters on the dice is important. Therefore, you should make 16 dice with the following sides:

- Die 1 - R, I, F, O, B, X
- Die 2 - I, F, E, H, E, Y
- Die 3 - D, E, N, O, W, S
- Die 4 - H, M, S, R, A, O
- Die 5 - L, U, P, E, T, S
- Die 6 - A, C, I, T, O, A
- Die 7 - Y, L, G, K, U, E
- Die 8 - Qu, B, M, J, O, A
- Die 9 - E, H, I, S, P, N
- Die 10 - V, E, T, I, G, N
- Die 11 - B, A, L, I, Y, T
- Die 12 - E, Z, A, V, N, D
- Die 13 - R, A, L, E, S, C
- Die 14 - U, W, I, L, R, G
- Die 15 - P, A, C, E, M, D
- Die 16 - U, T, O, K, N, D

Each die can fall into any of the 16 grid positions. In this version, players are given unlimited time to try to guess all words in the grid. The computer will keep track of all possible words and the maximum score that a player can earn. The player has the option to 'Give Up' once they can no longer identify any words and compare their score to the maximum possible score. Scoring of the game works as follows (based on word length):

- Fewer than 3 Letters: no score
- 3 Letters: 1 point
- 4 Letters: 1 point
- 5 Letters: 2 points
- 6 Letters: 3 points
- 7 Letters: 4 points
- 8 or More Letters: 11 points

For the die with Qu, this will count as two letters when determining score. 

## Overview of the Interface:

### Sample run of program

## Data Structures and Algorithms:

In the case of your program, words should be kept in an unordered set from the C++ STL. You can find more details on this in the additional requirements. 

## Code Organization:

You will need to make sure that your code meets the following specifications.
Note that there is some room for interpretation, but a general code outline is given below.

## Additional Requirements:

Your application must function as described below:

1. Your program must adhere to the class diagrams provided in this description.
2. You program must adhere to using the given interface as specified.
3. You must implement a backtracking algorithm to find all legal words. Your legal words will be stored in an unordered set. You can use the unordered set data structure from the standard template library in C++ (example, https://www.geeksforgeeks.org/unordered_set-in-cpp-stl/). You should not use any other data structure to store your words. 

## Important Notes:

- Projects will be graded on whether they correctly solve the problem, and whether they adhere to good programming practices.
- Projects must be received by the time specified on the due date. Projects received after that time will get a grade of zero.
- Do not change the test files unless told to! The results you get will be pointless as they will not align with our grading!
- Please review the academic honesty policy.
  - Note that viewing another student's solution, whether in whole or in part, is considered academic dishonesty.
  - Also note that submitting code obtained through the Internet or other sources, whether in whole or in part, is considered academic dishonesty. \* All programs submitted will be reviewed for evidence of academic dishonesty, and all violations will be handled accordingly.
  
## Breakdown of Grades:

You will find a rubric for the project in Canvas. 

## Submission Instructions:

1. All code must be added and committed to your local git repository.
2. All code must be pushed to the GitHub repository created when you "accepted" the assignment.
   1. After pushing, with `git push origin master`, visit the web URL of your repository to verify that your code is there.
      If you don't see the code there, then we can't see it either.
3. Your code must compile and run in Travis-CI or it might not be graded.
   1. The Travis-CI build should begin automatically when you push your code to GitHub.
   2. If your program will not compile, the graders will not be responsible for trying to test it.
   3. You should get an email regarding the status of your build, if it does not pass, keep trying.
