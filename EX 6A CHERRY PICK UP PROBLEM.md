# EX 6A CHERRY PICK UP PROBLEM

## AIM:
To Create a python program for the following problem statement.
You are given an n x n grid representing a field of cherries, each cell is one of three possible integers.
0	means the cell is empty, so you can pass through,
1	means the cell contains a cherry that you can pick up and pass through, or
-1 means the cell contains a thorn that blocks your way.
Return the maximum number of cherries you can collect by following the rules below:
Starting at the position (0, 0) and reaching (n - 1, n - 1) by moving right or down through valid path cells (cells with value 0 or 1).
After reaching (n - 1, n - 1), returning to (0, 0) by moving left or up through valid path cells.
When passing through a path cell containing a cherry, you pick it up, and the cell becomes an empty cell 0. If there is no valid path between (0, 0) and (n - 1, n - 1), then no cherries can be collected.



## Algorithm
Start the program.

Initialize the grid (2D matrix) where:

Positive values = number of cherries in a cell.

-1 (if present) = invalid/blocked cells (to be avoided).

Define recursive function dp(i, j, k) with memoization, where:

i = current row.

j = column of first robot.

k = column of second robot.

Base case: if i is the last row, return collected cherries (grid[i][j] + grid[i][k] if j != k).

Otherwise, compute cherries from current cells.

Try all 9 combinations of moves (robots can move left, down, or right diagonally).

Keep the maximum cherries collected.

Store result in memo to avoid recomputation.

Start recursion with both robots at row 0: one at column 0, the other at column COL_NUM - 1.

Return the maximum cherries collected.

Print the result.

Stop the program.  

## Program:
```
/*
To implement the program for Cherry pickup problem.


Developed by: Dinesh M
Register Number: 212222040039

class Solution(object):
    def cherryPickup(self, grid):
        def dp(i, j, k):
            if (i, j, k) in memo:
                return memo[(i, j, k)]
            
            if i == ROW_NUM - 1:
                return grid[i][j] + (grid[i][k] if j != k else 0)
            
            cherries = grid[i][j] + (grid[i][k] if j != k else 0)
            
            max_cherries = 0
            for dj in [-1, 0, 1]:
                for dk in [-1, 0, 1]:
                    next_j, next_k = j + dj, k + dk
                    if 0 <= next_j < COL_NUM and 0 <= next_k < COL_NUM:
                        max_cherries = max(max_cherries, dp(i + 1, next_j, next_k))
            
            memo[(i, j, k)] = cherries + max_cherries
            return memo[(i, j, k)]
        
        ROW_NUM = len(grid)
        COL_NUM = len(grid[0])
        memo = {}
        return dp(0, 0, COL_NUM - 1)

grid=[[0,1,-1],[1,0,-1],[1,1,1]] 
obj=Solution()
print(obj.cherryPickup(grid)+3)



*/
```

## Output:
<img width="1276" height="407" alt="Screenshot 2025-09-07 191407" src="https://github.com/user-attachments/assets/8b11328e-e434-46a9-b26e-7efdbfd27e6f" />



## Result:
Thus the above program was executed successfully for finding the maximum number of cherries from grid.
