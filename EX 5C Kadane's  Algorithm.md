# EX 5C Kadane's Algorithm
## DATE: 22/04/25
## AIM:
To write a python program to find the maximum contiguous subarray.

## Algorithm
1. Input: n (number of elements), a[] (list of integers)
2. Initialize max_so_far = a[0]
3. Initialize max_ending_here = 0
4. For i = 0 to n - 1:
Add a[i] to max_ending_here
5. If max_ending_here < 0:
6. Set max_ending_here = 0
7. Else if max_so_far < max_ending_here:
8. Set max_so_far = max_ending_here
9. Return max_so_far  

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
def maxSubArraySum(a,size):
    #####################  Add your Code here #############
    #Start here
    max_so_far = a[0]
    max_ending_here = 0
    for i in range(0, size):
        max_ending_here = max_ending_here + a[i]
        if max_ending_here < 0:
            max_ending_here = 0
        elif (max_so_far < max_ending_here):
            max_so_far = max_ending_here
              
    return max_so_far
    #End here
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:

![image](https://github.com/user-attachments/assets/c921d312-f082-4dd3-881a-539867f932d7)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
