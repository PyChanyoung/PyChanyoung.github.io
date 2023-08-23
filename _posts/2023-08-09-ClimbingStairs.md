---
layout: single
title: "Leetcode(Easy) - Climbing Stairs"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

You are climbing a staircase. It takes `n` steps to reach the top.

Each time you can either climb `1` or `2` steps. In how many distinct ways can you climb to the top?

<**Example 1**>

```
Input: n = 2
Output: 2
Explanation: There are two ways to climb to the top.
1. 1 step + 1 step
2. 2 steps
```

<**Example 2**>

```
Input: n = 3
Output: 3
Explanation: There are three ways to climb to the top.
1. 1 step + 1 step + 1 step
2. 1 step + 2 steps
3. 2 steps + 1 step
```

<**Constraints**>

- `1 <= n <= 45`

## Solution

```python
# Using DP
class Solution:
    def climbStairs(self, n: int) -> int:
        if n == 1:
            return 1
        if n == 2:
            return 2
        dp = [0] * n
        dp[0] = 1
        dp[1] = 2
        for i in range(2, n):
            dp[i] = dp[i-2] + dp[i-1]
        return dp[n-1]

# Using Memoize
class Solution:
    def climbStairs(self, n: int) -> int:
        def helper(memoize, cur):
            if cur in memoize:
                return memoize[cur]
            else:
                newVal = helper(memoize, cur-1) + helper(memoize, cur-2)
                memoize[cur] = newVal
                return newVal
        return helper({1:1, 2:2}, n)

# Best Solution
class Solution:
    def climbStairs(self, n: int) -> int:
        lastTwo = [1, 2]
        count = 2
        while count < n:
            lastTwo[0], lastTwo[1] = lastTwo[1], lastTwo[0] + lastTwo[1]
            count += 1
        return lastTwo[1] if n != 1 else 1
```

## Description

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)
