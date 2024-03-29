---
layout: single
title: "Leetcode(Easy) - Happy Number"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Write an algorithm to determine if a number `n` is happy.

A **happy number** is a number defined by the following process:

- Starting with any positive integer, replace the number by the sum of the squares of its digits.
- Repeat the process until the number equals 1 (where it will stay), or it **loops endlessly in a cycle** which does not include 1.
- Those numbers for which this process **ends in 1** are happy.
  Return `true` _if_ `n` _is a happy number, and_ `false` _if not._

<**Example 1**>

```
Input: n = 19
Output: true
Explanation:
1^2 + 9^2 = 82
8^2 + 2^2 = 68
6^2 + 8^2 = 100
1^2 + 0^2 + 0^2 = 1

```

<**Example 2**>

```
Input: n = 2
Output: false
```

<**Constraints**>

```
1 <= n <= 2^31 - 1
```

## Solution

```python
# 1
class Solution:
    def isHappy(self, n: int) -> bool:
        visit = set()
        while n != 0 and n not in visit:
            visit.add(n)
            output = 0
            while n > 0:
                digit = n % 10
                digit = digit ** 2
                output += digit
                n = n // 10
            n = output
        return n == 1

# 2(Optimized)
class Solution:
    def isHappy(self, n: int) -> bool:
        visit = set()
        while n != 0 and n not in visit:
            visit.add(n)
            n = self.sumOfDigits(n)
        return n == 1

    def sumOfDigits(self, n: int) -> int:
        output = 0
        while n > 0:
            digit = n % 10
            digit = digit ** 2
            output += digit
            n = n // 10
        return output

# 3(Best optimized)
class Solution:
    def isHappy(self, n: int) -> bool:
        visit = set()
        while n != 1 and n not in visit:
            visit.add(n)
            n = sum(int(i) ** 2 for i in str(n))
        return n == 1
```

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)
