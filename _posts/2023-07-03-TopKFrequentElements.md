---
layout: single
title: "Leetcode(Medium) - Top K Frequent Elements"
categories: CodingInterview
tag: [Python, Algorithm, Coding]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given an integer array `nums` and an integer `k`, return _the `k` most frequent elements_. You may return the answer in **any order**.

<**Example 1**>

```
Input: nums = [1,1,1,2,2,3], k = 2
Output: [1,2]

```

<**Example 2**>

```
Input: nums = [1], k = 1
Output: [1]
```

<**Constraints**>

- `1 <= nums.length <= 10^5`
- `-10^4 <= nums[i] <= 10^4`
- `k` is in the range `[1, the number of unique elements in the array]`.
- It is **guaranteed** that the answer is **unique**.

## Solution

```python
# Time Complexity: O(klogN)
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]:
        my_dic = {}
        res = []

        for num in nums:
            my_dic[num] = 1 + my_dic.get(num, 0)

        heap = [(-value, key) for key, value in my_dic.items()]
        heapq.heapify(heap)

        for _ in range(k):
            value, key = heapq.heappop(heap)
            res.append(key)

        return res

# Time Complexity: O(n)
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]:
        my_dic = {}
        frequent = [[] for i in range(len(nums) + 1)]

        for num in nums:
            my_dic[nums] = 1 + my_dic.get(num, 0)

        for value, count in my_dic.items():
            frequent[count].append(value)

        result = []
        for idx in range(len(freq)-1, 0, -1):
            for value in freq[idx]:
                result.append(value)
                if len(result) == k:
                    return result
```

## Time/Space Complexity

- Time Complexity: O(n)
- Space Complexity: O(n)
