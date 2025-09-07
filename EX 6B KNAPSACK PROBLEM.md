# EX 6B KNAPSACK PROBLEM

## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.



## Algorithm
Start the program.

Input:

x → number of value inputs

y → number of weight inputs

W → capacity of the knapsack

val[] → list of values of items

wt[] → list of weights of items

Define function knapSack(W, wt, val, n) that:

Initialize a 2D DP table K[n+1][W+1] with zeros.

For i in 0 to n (items) and w in 0 to W (capacity):

If i == 0 or w == 0, set K[i][w] = 0.

Else if wt[i-1] <= w, set:

Else, set K[i][w] = K[i-1][w].

Return K[n][W] → the maximum value for n items and capacity W.

Call knapSack(W, wt, val, n) and print the result.

Stop the program.

## Program:
```
/*
To implement the program for 0/1 knapsack problem.


Developed by: Dinesh M
Register Number: 212222040039

def knapSack(W, wt, val, n):
    ########## Add your code here #########
    K = [[0 for x in range(W + 1)] for x in range(n + 1)]
    for i in range(n + 1):
        for w in range(W + 1):
            if i == 0 or w == 0:
                K[i][w] = 0
            elif wt[i-1] <= w:
                K[i][w] = max(val[i-1]+ K[i-1][w-wt[i-1]],K[i-1][w])
            else:
                K[i][w] = K[i-1][w]
 
    return K[n][W]

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))

n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
*/
```

## Output:
<img width="1226" height="734" alt="Screenshot 2025-09-07 191619" src="https://github.com/user-attachments/assets/5066e82e-f611-4575-aca4-e20e61aac9b7" />



## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
