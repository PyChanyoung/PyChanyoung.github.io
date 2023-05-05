---
layout: single
title: "Blind75 - Maximum Depth of Binary Tree"
categories: CodingInterview
tag: [Python, Algorithm, Coding, Blind75]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given the `root` of a binary tree, return its maximum depth.

A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

<**Example 1**>

```
         3
       /   \
      9    20
           / \
          15  7
Input: root = [3,9,20,null,null,15,7]
Output: 3
```

<**Example 2**>

```
         1
       /   \
            2
Input: root = [1,null,2]
Output: 2
```

<**Constraints**>

- The number of nodes in the tree is in the range `[0, 10^4]`.
- `-100 <= Node.val <= 100`
