---
layout: single
title: "Leetcode(Medium) - Two Sum II - Input Array Is Sorted"
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

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(1)
