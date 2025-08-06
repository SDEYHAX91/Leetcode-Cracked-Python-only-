# Richest Customer Wealth 🚀

## 🧠 Problem Statement
You are given an **m x n** integer grid **accounts** where **accounts[i][j]** is the amount of money the **i​​​​​​​​​​​th​​​​ customer** has in the **j​​​​​​​​​​​th​​​​ bank**. Return the wealth that the **richest customer** has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

A running sum is defined as:  
`runningSum[i] = sum(nums[0]…nums[i])`

## Examples:
**1.**

**Input:** accounts = [[1,2,3],[3,2,1]]

**Output:** 6

**Explanation:**

'1st customer has wealth = 1 + 2 + 3 = 6'

2nd customer has wealth = 3 + 2 + 1 = 6

Both customers are considered the richest with a wealth of 6 each, so return 6.


**2.**

**Input:** accounts = [[1,5],[7,3],[3,5]]

**Output:** 10

**Explanation:** 

1st customer has wealth = 6

2nd customer has wealth = 10 

3rd customer has wealth = 8

The 2nd customer is the richest with a wealth of 10.

---

## ✅ Approach

1. Initialize a variable `sum = 0`.
2. Iterate through the array once.
3. At each index, add the current number to `sum`.
4. Replace the current element with the new `sum` (i.e., do it **in-place**).
5. Return the modified `nums` array.

---

## 🧮 Complexity

| Type              | Value     |
|-------------------|-----------|
| Time Complexity   | `O(n)`    |
| Space Complexity  | `O(1)`    |

⚠ Note:  
Even though this solution uses **O(1)** extra space and is **in-place**, LeetCode’s leaderboard may not reflect it due to:
- Memory reporting includes input/output arrays.
- Python interpreter overhead.
- Implementation-level optimizations in other languages.

---

## 🔍 Code (Python)

```python
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        sum = 0
        for i in range(len(nums)):
            sum += nums[i]
            nums[i] = sum
        return nums
