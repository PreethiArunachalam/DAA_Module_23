# EX 5B Coin Change Problem
## DATE: 19/04/05
## AIM:
To compute the fewest number of coins that we need to make up the amount given.

## Algorithm
1. Input: n (number of coin types), s[] (list of coin denominations), amt (target amount)
2. Initialize a list dp of size amt + 1 with all values as ∞ (infinity)
3. Set dp[0] = 0 (0 coins needed to make amount 0)
4. For each coin in s:
For i = coin to amt:
5. Update dp[i] = min(dp[i], dp[i - coin] + 1)
6. If dp[amt] is still ∞, return -1 (amount can't be formed)
7. Else, return dp[amt] (minimum number of coins needed)  

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
class Solution(object):
   def coinChange(self, coins, amount):
       ####################      Add your Code Here ###########
        dp = [float('inf')] * (amount + 1)
        dp[0]=0
        for coin in coins:
            for i in range(coin, amount + 1):
                dp[i] = min(dp[i], dp[i - coin] + 1)
        return dp[amount] if dp[amount]!=float('inf') else -1
      
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```
## Output:

![image](https://github.com/user-attachments/assets/5a905abd-17f2-4add-a767-be9c92641f2c)

## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
