---
layout: single
title: "Leetcode(Medium) - Generate Parentheses"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given `n` pairs of parentheses, write a function to _generate all combinations of well-formed parentheses_.

<**Example 1**>

```
Input: n = 3
Output: ["((()))","(()())","(())()","()(())","()()()"]
```

<**Example 2**>

```
Input: n = 1
Output: ["()"]
```

<**Constraints**>

- `1 <= n <= 8`

## Solution

```
class Solution:
    def generateParenthesis(self, n: int) -> List[str]:
        stack = []
        answer = []

        def backtrack(openN, closedN):
            if openN == closedN == n:
                answer.append("".join(stack))
                return

            if openN < n:
                stack.append("(")
                backtrack(openN + 1, closedN)
                stack.pop()

            if closedN < openN:
                stack.append(")")
                backtrack(openN, closedN + 1)
                stack.pop()

        backtrack(0, 0)
        return answer
```

## Description

## Time/Space Complexity

- Time Complexity:
- Space Complexity:
