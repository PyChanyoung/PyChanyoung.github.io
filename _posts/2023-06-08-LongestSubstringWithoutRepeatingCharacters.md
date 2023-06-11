---
layout: single
title: "Leetcode(Medium) - Longest Substring Without Repeating Characters"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given a string, find the length of **longest substring** without repeating characters.

<**Example 1**>
```
Input: "abcabcbb"
Output: 3
Explanation: The answer is "abc", with the length of 3.
```
<**Example 2**>
```
Input: s = "bbbbb"
Output: 1
Explanation: The answer is "b", with the length of 1.
```
<**Example 3**>
```
Input: s = "pwwkew"
Output: 3
Explanation: The answer is "wke", with the length of 3.
Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.
```

## Solution
```
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        charSet = set()
        l = 0
        res = 0
        for r in range(len[s]):
            while s[r] in charSet:
                charSet.remove(s[l])
                l += 1
            charSet.add(s[r])
            res = max(res, r - l + 1)
        return res
```

## Time/Space Complexity
- Time Complexity: O(n)
- Space Complexity: O(1)
