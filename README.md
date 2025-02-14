
The Simplex Algorithm is an iterative method for solving linear programming optimization problems. This program is designed to handle a problem involving 10 decision variables, which could represent a group of 10 students in a project where each student's contribution might need to be optimized. The goal here is to demonstrate how the Simplex Algorithm can be implemented in C++ for a relatively larger set of variables.

Implementation Details:

Data Structure:
A 2D vector is used to represent the tableau. The first row represents the objective function, and subsequent rows represent constraints. This implementation extends to 10 decision variables (x1 to x10) and includes slack variables for equality constraints.
Functions:
findPivotColumn: This function identifies the variable that should enter the basis by finding the most negative coefficient in the objective function (ignoring the constant term).
findPivotRow: Executes the minimum ratio test to find which variable should leave the basis, ensuring the solution remains feasible.
pivot: Performs the pivot operation, which involves normalizing the pivot row and adjusting other rows accordingly.
isOptimal: Checks if the current solution is optimal by ensuring no negative coefficients exist in the objective function row (except the constant).
printTableau: Useful for debugging and visualization, prints the current state of the tableau.
displaySolution: After finding the optimal solution, this function extracts and displays the values of the decision variables.
Main Loop:
The main function sets up a simple linear programming problem with 10 variables and 2 constraints as an example. The loop continues until an optimal solution is found by repeatedly selecting a pivot column and row, performing the pivot, and checking for optimality.
Solution Extraction:
The solution is extracted by identifying where each decision variable has a coefficient of 1 in any constraint row, indicating its basic variable status.

Assumptions and Limitations:
This implementation assumes all variables are non-negative and constraints are in equality form. For real-world scenarios, additional preprocessing might be needed to convert inequalities.
The example provided is simplistic; real-world problems might require handling degeneracy, artificial variables for initial feasible solutions, or more complex constraints.

Enhancements for Group Work:
For educational purposes with a group of 10 students, this program could be extended:
To allow input from each student for their constraints or contributions.
To include interactive elements where students can see how different constraints affect the solution.
To integrate with a user interface or file I/O for reading problem definitions from files created by students.

Conclusion:
This program demonstrates the application of the Simplex Algorithm in C++ for a scenario involving 10 decision variables, suitable for a group project scenario. It serves as an educational tool to understand linear programming and the Simplex method. For practical use, further robustness and error handling would be necessary.
