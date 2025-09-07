# EX 6C TRAVELLING SALES MAN PROBLEM

## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm
Start the program.

Input the graph as a 2D adjacency matrix graph[V][V], where V is the number of vertices.

Choose the starting vertex s.

Generate a list vertex[] of all vertices except the starting vertex.

Use itertools.permutations to generate all possible orderings of vertices.

Initialize min_path = ∞.

For each permutation:

Compute the total path weight starting from s, visiting all vertices in the permutation, and returning to s.

Update min_path if the computed path weight is smaller.

Return min_path as the minimum cost of the TSP.

Print the result.

Stop the program.  

## Program:
```
/*
To implement the program for TSP.


Developed by: Dinesh M
Register Number: 212222040039

from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
    ##Write your code
    vertex = [] 
    for i in range(V): 
        if i != s: 
            vertex.append(i) 
    min_path = maxsize 
    next_permutation=permutations(vertex)
    for i in next_permutation:

        current_pathweight = 0
        k = s 
        for j in i: 
            current_pathweight += graph[k][j] 
            k = j 
        current_pathweight += graph[k][s] 
        min_path = min(min_path, current_pathweight) 
         
    return min_path
   
 
 

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s)) 
*/
```

## Output:
<img width="1342" height="347" alt="Screenshot 2025-09-07 191758" src="https://github.com/user-attachments/assets/eac2c5f7-624d-49e7-b490-e3ab929853ba" />



## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
