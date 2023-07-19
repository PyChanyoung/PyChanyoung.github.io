---
layout: single
title: "Leetcode(Medium) - Find The Duplicate Number"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given an array of integers `nums` containing `n + 1` integers where each integer is in the range `[1, n]` inclusive.

There is only **one repeated number** in `nums`, return _this repeated number_.

You must solve the problem **without** modifying the array `nums` and uses only constant extra space.

<**Example 1**>

```
Input: nums = [1,3,4,2,2]
Output: 2
```

<**Example 2**>

```
Input: nums = [3,1,3,4,2]
Output: 3
```

<**Constraints**>

- `1 <= n <= 10^5`
- `nums.length == n + 1`
- `1 <= nums[i] <= n`
- All the integers in `nums` appear only **once** except for **precisely one integer** which appears **two or more** times.

**Follow up:**

- How can we prove that at least one duplicate number must exist in `nums`?
- Can you solve the problem in linear runtime complexity?

## Solution

```
class Solution:
    def findDuplicate(self, nums: List[int]) -> int:
        tortoise, hare = 0, 0
        while True:
            tortoise = nums[tortoise]
            hare = nums[nums[hare]]
            if tortoise == hare:
                break # from beginning of cycle to intersection of the tortoise and the hare

        tortoise = 0
        while True:
            tortoise = nums[tortoise] # -> p
            hare = nums[hare] # -> k
            if tortoise == hare:
                return tortoise
```

## Description

We can use the Floyd's Tortoise and Hare Algorithm to solve this problem.</br>
Rationale: Given an array of length n+1 with elements ranging from 1 to n, and there is one repeated number.</br>
Floyd's Tortoise and Hare in other words Cycle Detection algorithm can be used to find a cycle in a linked list or an array.</br>
Initially, the tortoise and hare are at the starting point. The tortoise moves one step at a time and the hare moves two steps at a time.</br>
The point at which the tortoise and the hare meet is somewhere inside the cycle.</br>

```
indices	: 0 1 2 3 4
numbers	: 1 3 4 2 2
idx:0/val:1 -> idx:1/val:3 -> idx:3/val:2 -> idx:2/val:4 <-> idx:4/val:2
```

Let's check it out mathematically.</br>
According to the algorithm, 2*Tortoise = Hare.</br>
`p` is the distance from the starting point to the beginning of the cycle.</br>
`c` is the length of the cycle.</br>
`x` is the distance from the intersection where tortoise and hare meet to the beginning of the next cycle.</br>
At the point of intersection, the total distance the tortoise has moved is p + c - x.</br>
The hare, moving twice as fast, has moved a total distance of p + 2c - x.</br>
By setting 2*Tortoise = Hare, we get 2(p+c-x) = p+2c-x.</br>
Simplifying, we find that p = x.</br>
Since this formula proves that p and x are equal, if one pointer is moved back to the starting point after the two pointers meet, and then both pointers are moved the same distance, they will meet at the duplicated number, which is also the starting point of the cycle.</br>

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(1)
