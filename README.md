# cs1302-ce26 Tic-Tac-Toe Solver

This class exercise futher explores the concept of [recursion](https://github.com/cs1302uga/cs1302-ce26).

You will write a method to print all possible Tic-Tac-Toe boards from a given starting point. Some helpful
utility methods are provided for you in the starter code contained in the provided Maven project.

## Course-Specific Learning Outcomes
* **LO2.c:** Use recursion to solve a non-trivial problem in a software solution.
* **LO3.d:** Apply pair-programming principles in a software-based project.

## References and Prerequisites

* [`CSCI 1302 Recursion Tutorial`](https://github.com/cs1302uga/cs1302-tutorials/blob/master/recursion.md)

## Questions

In your notes, clearly answer the following questions. These instructions assume that you are 
logged into the Nike server. 

**NOTE:** If a step requires you to enter in a command, please provide in your notes the full 
command that you typed to make the related action happen. If context is necessary (e.g., the 
command depends on your present working directory), then please note that context as well.

### Getting Started

1. **Let's do some pair programming!** Team up with one other person and make sure you only have one 
   laptop out. We recommend that use Comte de Rochambeau's technique to determine who gets to
   be the driver.
   
   > Comte de Rochambeau was a French nobleman who fought against the British during the Revolutionary War.
   > His name served as a codeword at the battle of Yorktown, where he commanded the French troops.
   > Legend has it that Comte de Rochambeau made decisions using a technique known as _roshambo_
   > or _rock, paper, scissors_. 
   > **-- A Legend told by Some Old, Wise Person**

1. Use Git to clone the repository for this exercise onto Nike into a subdirectory called `cs1302-ce26`:

   ```
   $ git clone --depth 1 https://github.com/cs1302uga/cs1302-ce26.git
   ```

1. Change into the `cs1302-ce26` directory that was just created and look around. There should be
   multiple Java files contained within the directory structure. To see a listing of all of the 
   files under the `src` subdirectory, use the `find` command as follows:
   
   ```
   $ find src
   ```
   
## Exercise Steps

1. While looking in the `src` directory, you likely saw a file called `TTTUtility.java`. 
   This file contains a Tic-Tac-Toe utility class with some helpful methods.
   Take a few minutes to familiarize yourselves with the documentation for these methods 
   using the documentation found here: 
   [TTT Utility](http://cobweb.cs.uga.edu/~barnes/cs1302-ttt/)

1. Take a few more minutes to read through `TTTSolver.java`. This file contains a `main` method
   which takes in an encoding for a game board. It then passes this game board to `printAllBoards`. 
   We will implement `printAllBoards` soon. For now, it simply prints the current game board.

1. **Next, use Maven to compile and run the code.**. Please use the `exec:java` phase with
   the `-Dexec.mainClass` option to run. The program should ask you to enter a game board.
   Enter a valid game board and make sure the board is printed to the screen before moving 
   on.
   
   * Once you get the code to compile and run, please write down the commands you used
     in your notes.
   
1. Pair Program:

   * **Current Pair Programming Driver (person typing)**: Open the `TTTUtility.java` file
     and implement the `isCat` method. The method takes a `String` reference to the current
     game board. Note: a game is a _cat game_ (or tie) if all spaces are full and neither `'X'`
     nor `'O'` has won the game. To simplify your implementation, use the methods already 
     present in `TTTUtility`.
   
   * **Current Pair Programming Rider**: Stay actively engaged with your group member while
     they are working. Offer suggestions and point out typos or logical errors as they work. 

1. Add a line to the `printAllBoards` method in `TTTSolver.java` to print `true` if the
   specified game board is a tie and `false` otherwise. You should use the `isCat` method
   that you wrote in the previous step.
   
1. After you've confirmed that the code compiles and runs, please add and commit
   your changes to the repository.

**CHECKPOINT**

1. **Swap drivers.** Consider a recursive implementation for the `printAllBoards` method in `TTTSolver`.

   * Identify the base case(s). Give an example.
   
   * Identify the recursive case(s).
   
   * Draw the recursion tree for `printAllBoards("XOXOXO---")`.

1. The group member who is currently driving (not the same person who implemented `isCat`): 
   implement the `printAllBoards` method in `TTTSolver`. The rider should be actively engaged
   in the process as well.

1. Use Maven to compile and run the code. After you've confirmed that it compiles and runs, 
   please add and commit your changes to the repository.

**CHECKPOINT**

1. **Swap drivers.** Implement a new method in `TTTSolver` called `countAllWinningBoards`
   that, given an initial board state and a player, returns a count of all winning board states
   for that player that can be reached via a valid sequence of moves by each player. Here is
   the signature for the method to help you get started:
   
   ```java
   int countAllWinningBoards(String board, char player)
   ```

   Remember, the rider should be actively engaged in the process as well.
   
1. Use Maven to compile and run the code. After you've confirmed that it compiles and runs, 
   please add and commit your changes to the repository.

**CHECKPOINT**

<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
