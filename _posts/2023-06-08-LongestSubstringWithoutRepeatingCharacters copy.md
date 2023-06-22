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
        myCharSet = set()  # Using a Set data structure to find duplicates.
        count = 0  # Keep updating a number as we go along and return this number.
        idx_1 = 0  # Two indices (idx_1, idx_2) are used to remove repeating characters when traversing the string with one index, starting from 0, and a duplicate occurs.
        for idx_2 in range(len(s)):
            while s[idx_2] in myCharSet:  # Using 'while' instead of 'if' because duplicates can occur multiple times.
                myCharSet.remove(s[idx_1])  # We know through the conditional statement that s[idx_2] already exists in myCharSet, and we know that s[idx_1] is the same as s[idx_2]. Since the outer loop progresses linearly to the right, we need to remove s[idx_1], which is located on the left side, to properly eliminate the duplicate character and continue searching for new duplicate characters.
                idx_1 += 1
            myCharSet.add(s[idx_2])
            count = max(count, idx_2 - idx_1 + 1)  # idx_2 - idx_1 + 1 represents the current size of the substring. idx_2 points to the rightmost index of the substring, and idx_1 points to the leftmost index. Therefore, idx_2 - idx_1 + 1 calculates the length of the substring.
        return count
```

## Time/Space Complexity
- Time Complexity: O(n)
- Space Complexity: O(1)
