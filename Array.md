# Must do Array Question.
### 1. Two Sum
 > Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
 > You may assume that each input would have exactly one solution, and you may not use the same element twice.

 ```Approach:```

  The key to the problem is that there is ALWAYS only 1 pair of numbers that satisfy the condition of adding together to be the target value.
  
  We can assume that for all the numbers in the list (x1, x2, ... xn) that there exists a pair such that xi + xj = target.
  
  To solve this with a single pass of the list we can change the equation above to xi = target - xj, since we know the target as long as we maintain a record of all previous values in the list we can compare the current value (xi) to it's ONLY pair, if it exists, in record of all previous values (xj).

  To keep a record of the previous values and their indices ***i*** we can use a dictionary. Commonly known as a map in other languages. This allows me to record each previous number in the dictionary alongside the indice as a key value pair (target-number, indice).
  
### 2. Best time to Buy and Sell
  > You are given an array prices where prices\[i] is the price of a given stock on the ith day.
  > You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.
  > Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

  ```Appraoch:```
  
   to be continued...
  
