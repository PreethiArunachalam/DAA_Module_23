# EX 5D Minimum Jump to Reach End Array
## DATE: 26/04/25
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm
1. Input: n (length of array), arr[] (array elements)
2. If n == 0 or arr[0] == 0:
3. Return ∞ (cannot move from the first position)
4. Initialize a list jumps[] of size n
5. Set jumps[0] = 0 (no jump needed at the start)
6. For i = 1 to n - 1:
7. Set jumps[i] = ∞
8. For j = 0 to i - 1:
If i <= j + arr[j] and jumps[j] ≠ ∞:
9. Set jumps[i] = min(jumps[i], jumps[j] + 1)
10. Break the inner loop (found valid jump)
11. Return jumps[n-1] (minimum jumps to reach the last index)  

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
def minJumps(arr, n):
    ##########  Add your code here ##############
    #Start here
    jumps = [0 for i in range(n)]
    if (n == 0) or (arr[0] == 0):
        return float('inf')
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
    #End here
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))
```
## Output:

![image](https://github.com/user-attachments/assets/d1fbe89e-62a0-4192-a277-9a4522c27364)

## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
