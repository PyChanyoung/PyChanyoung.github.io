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
        if len(s1) > len(s2):
            return False

        s1_hashMap, s2_hashMap = [0] * 26, [0] * 26
        for i in range(len(s1)):
            s1_hashMap[ord(s1[i]) - ord('a')] += 1
            s2_hashMap[ord(s2[i]) - ord('a')] += 1

        matches = 0
        for i in range(26):
            matches += 1 if s1_hashMap[i] == s2_hashMap[i] else 0

        left = 0
        for right in range(len(s1), len(s2)):
            if matches == 26:
                return True

            index = ord(s2[right]) - ord('a')
            s2_hashMap[index] += 1
            if s1_hashMap[index] == s2_hashMap[index]:
                matches += 1
            elif s1_hashMap[index] + 1 == s2_hashMap[index]:
                matches -= 1

            index = ord(s2[left]) - ord('a')
            s2_hashMap[index] -= 1
            if s1_hashMap[index] == s2_hashMap[index]:
                matches += 1
            elif s1_hashMap[index] - 1 == s2_hashMap[index]:
                matchese -= 1

            left += 1

        return matches == 26
```

## Description

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(26\*n)
