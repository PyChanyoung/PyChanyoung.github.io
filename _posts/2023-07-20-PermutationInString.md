---
layout: single
title: "Leetcode(Medium) - Permutation in String"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given two strings `s1` and `s2`, return `true` _if_ `s2` _contains a permutation of_ `s1`_, or_ `false` _otherwise_.

In other words, return `true` if one of `s1`'s permutations is the substring of `s2`.

<**Example 1**>

```
Input: s1 = "ab", s2 = "eidbaooo"
Output: true
Explanation: s2 contains one permutation of s1 ("ba").
```

<**Example 2**>

```
Input: s1 = "ab", s2 = "eidboaoo"
Output: false
```

<**Constraints**>

- `1 <= s1.length, s2.length <= 10^4`
- `s1` and `s2` consist of lowercase English letters.

## Solution

```
class Solution:
    def checkInclusion(self, s1: str, s2: str) -> bool:
```

## Description

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(26\*n)
