---
layout: single
title: "Leetcode(Medium) - Longest Consecutive Sequence"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given an unsorted array of integers `nums`, return _the length of the longest consecutive elements sequence._

You must write an algorithm that runs in `O(n)` time.

<**Example 1**>

```
Input: nums = [100,4,200,1,3,2]
Output: 4
Explanation: The longest consecutive elements sequence is `[`1, 2, 3, 4]`. Therefore its length is 4.

```

<**Example 2**>

```
Input: nums = [0,3,7,2,5,8,4,6,0,1]
Output: 9
```

<**Constraints**>

- `0 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

## Solution

```python
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        numSet = set(nums)
        longest = 0
        for num in nums:
            if (num - 1) not in numSet:
                length = 0
                while (num - length) in numSet:
                    length += 1
                longest = max(longest, length)
        return longest
```

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)
