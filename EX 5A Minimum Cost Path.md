# EX 5A Minimum Cost Path
## DATE: 15/04/24
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm
1. Input: R (rows), C (columns)
2. Create a 2D array `tc[R][C]`
3. Set `tc[0][0] = cost[0][0]`
4. For `i = 1` to `m`: `tc[i][0] = tc[i-1][0] + cost[i][0]`
5. For `j = 1` to `n`: `tc[0][j] = tc[0][j-1] + cost[0][j]`
6. For `i = 1` to `m`:
7. For `j = 1` to `n`:
    `tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]`
8. Return `tc[m][n]`
  
## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
R = int(input())
C = int(input())
def minCost(cost, m, n):
 
    tc = [[0 for x in range(C)] for x in range(R)]
    tc[0][0] = cost[0][0]
    for i in range(1, m+1):
        tc[i][0] = tc[i-1][0] + cost[i][0]
    for j in range(1, n+1):
        tc[0][j] = tc[0][j-1] + cost[0][j]
    for i in range(1, m+1):
        for j in range(1, n+1):
            tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]
    return tc[m][n]
 
# Driver program to test above functions
cost = [[1, 2, 3],
        [4, 8, 2],
        [1, 5, 3]]
print(minCost(cost,2,2))
```
## Output:

![image](https://github.com/user-attachments/assets/6256c3f3-af68-4f9b-9afc-e399974e6bae)

## Result:
Thus the above program was executed successfully for finding the minimum cost.
