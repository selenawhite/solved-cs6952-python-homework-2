Download Link: https://assignmentchef.com/product/solved-cs6952-python-homework-2
<br>
<strong>Example Input File (same for all problems)</strong>

5 3 0 0 7 0 0 0 0 6 0 0 1 9 5 0 0 0 0 9 8 0 0 0 0 6 0 8 0 0 0 6 0 0 0 3 4 0 0 8 0 3 0 0 1 7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5 0 0 0 0 8 0 0 7 9

<ol>

 <li><strong> Reading Input: 20 points</strong></li>

</ol>

<strong>File: </strong>sudoku1.py

A Sudoku game is played on a 9×9 grid and starts at some initial valid state. To play, you have to read the initial configuration of a grid first. Since the player may want to choose a different starting grid for each game, you need to allow the user to type in the name of the file that contains the initial grid.

At the start of the program, prompt user for the file path using the input() function. Open the specified file and read its content. The file will contain a 9×9 grid of numbers separated by spaces; 1-9 are valid start numbers and 0 denotes empty cell. To verify that the grid was read correctly, print it out. You can assume the input will always be a valid Sudoku grid.

<strong>Console Session</strong>

Enter input filepath: input.txt

5 3 0 0 7 0 0 0 0 6 0 0 1 9 5 0 0 0 0 9 8 0 0 0 0 6 0 8 0 0 0 6 0 0 0 3 4 0 0 8 0 3 0 0 1 7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5 0 0 0 0 8 0 0 7 9

<ol start="2">

 <li><strong> Solving Sudoku: 20 points</strong></li>

</ol>

<strong>File: </strong>sudoku2.py

Read a Sudoku grid as before from the user-specified file. To play the Sudoku game, a user must be able to enter numbers into the grid. After you printed the initial grid, prompt the user for a row, column, and number, set the content of the cell at position (row, column) to value number and print the updated grid. The input will be a valid grid, and the row and column will be the index of a cell that is empty (one containing a 0).

<strong>Note: you will have to convert the number of the input grid to integers to update the values in the grid. Each cell should have numbers in 0-9 range (with 0 indicating an empty cell).</strong>

<strong>Console Session</strong>

Enter input filepath: input.txt

5 3 0 0 7 0 0 0 0 6 0 0 1 9 5 0 0 0 0 9 8 0 0 0 0 6 0 8 0 0 0 6 0 0 0 3 4 0 0 8 0 3 0 0 1 7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5

<h1>0 0 0 0 8 0 0 7 9</h1>

Enter row: 1

Enter column: 2

Enter number: 1

5 3 0 0 7 0 0 0 0 6 0 1 1 9 5 0 0 0

0 9 8 0 0 0 0 6 0

8 0 0 0 6 0 0 0 3

4 0 0 8 0 3 0 0 1

7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5 0 0 0 0 8 0 0 7 9

<ol start="3">

 <li><strong> Validating Steps: 20 points</strong></li>

</ol>

<strong>File: </strong>sudoku3.py

You can assume that the input entered by the user is in a valid range: row and column are in the 0-8 range, and number is in the 0-9 range. In this exercise, you need to check if the input constitutes a valid step in solving the Sudoku based on the rules of the game.

<table width="360">

 <tbody>

  <tr>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

  </tr>

  <tr>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

  </tr>

  <tr>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

  </tr>

  <tr>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

  </tr>

  <tr>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

  </tr>

  <tr>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

  </tr>

  <tr>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"> </td>

  </tr>

  <tr>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

  </tr>

  <tr>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"> </td>

   <td width="40"> </td>

   <td width="40"></td>

   <td width="40"></td>

  </tr>

 </tbody>

</table>

Figure 1: Example of Sudoku grid which consists of nine 3×3 subgrids (source Wikipedia).

A valid configuration to the Sudoku grid must satisfy following rules:

<ul>

 <li>each cell has a number in the 0-9 range</li>

 <li>in each row, no number in the range 1-9 can be repeated</li>

 <li>in each column, no number in the range 1-9 can be repeated</li>

 <li>in each 3×3 subgrid, no number in the range 1-9 can be repeated For example, entering number 3 at row 0 and column 2 will violate both the row rule and the subgrid rule.</li>

</ul>

In this exercise, read the starting Sudoku configuration by prompting a user for the file path as in part 1 or 2. When user enters a new number that violates the Sudoku rules print a message containing the rule that was broken (‘Number X twice in row’, ‘Number X twice in column’, or ‘Number X twice in subgrid’; <strong>check and print them in this order</strong>) and do not update the grid. If the number does not break any rule, update the grid and print it.

<strong>Console Session</strong>

Enter input filepath: input.txt

5 3 0 0 7 0 0 0 0 6 0 0 1 9 5 0 0 0 0 9 8 0 0 0 0 6 0 8 0 0 0 6 0 0 0 3 4 0 0 8 0 3 0 0 1 7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5

0 0 0 0 8 0 0 7 9

Enter row: 1

<h1>Enter column: 2</h1>

Enter number: 1

Number 1 twice in row

<h1>5 3 0 0 7 0 0 0 0 6 0 0 1 9 5 0 0 0</h1>

0 9 8 0 0 0 0 6 0

<h1>8 0 0 0 6 0 0 0 3</h1>

4 0 0 8 0 3 0 0 1 7 0 0 0 2 0 0 0 6

0 6 0 0 0 0 2 8 0 0 0 0 4 1 9 0 0 5 0 0 0 0 8 0 0 7 9

<ol start="4">

 <li><strong>Grid GUI: 20 points</strong></li>

</ol>

<strong>File: </strong>sudoku4.py

In the quest for building a user-friendly Sudoku application, we have to create GUI as most users dislikes console. In this part, you need to write Qt program that constructs a 9×9 grid consisting of nine 3×3 subgrids. Cells in the subgrids should be combo boxes that allow the user to select a number (see code presented in class for example). Read the input file and fill the GUI with the initial grid. The user can perform moves using the combo boxes in the GUI but you are not required to check for the validity of the moves based on Sudoku rules.

Figure 2: Example Sudoku GUI

<ol start="5">

 <li><strong>Validation and Hints in GUI: 20 points</strong></li>

</ol>

<strong>File: </strong>sudoku5.py

Anybody doing Sudoku on paper knows that it is quite suboptimal experience, but we use computers and sky is the limit. Enhance the Sudoku GUI and check for the three rules. If the user makes a mistake, show a message with the specifics of the mistake and revert back to the previous value in the grid cell.

You need to check these rules:

<ul>

 <li>in each row, no number in the range 1-9 can be repeated</li>

 <li>in each column, no number in the range 1-9 can be repeated</li>

 <li>in each 3×3 subgrid, no number in the range 1-9 can be repeated Moreover, it is common to write down the possible numbers for each cell when solving Sudoku on paper. Modify your code so that each empty combo box shows only the list of valid numbers from the range 1-9. For each non-empty combo box show only the option to maintain the current value or clear the cell. For example, the possible choices that do not violate any of the rules in row 0 and column 2 are 1, 2, and 4. Similarly, for row 3 and column 3 the user should only have the two options of clearing the cell or maintaining the value 8.</li>

</ul>