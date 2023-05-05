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

## Solution

```
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def maxDepth(self, root: Optional[TreeNode]) -> int:
        def maxDepthHelper(node, maximumDepth):     # A helper method is used to open a stack while computing the maximum depth.
            if node is None:                        # If input is Null,
                return maximumDepth                 # Return the value of the maximumDepth computed so far.
            maximumDepth += 1                       # If input is not Null,
            return max(maxDepthHelper(node.left, maximumDepth),
            maxDepthHelper(node.right, maximumDepth))   # Open the left and right stacks and invoke recursion inside them. Then, at the point when the stacks are closing, each helper method returns its value, and when all stacks are closed, the values returned by the left and right stacks, up to that point, are compared.

        return maxDepthHelper(root, 0)              # Return the value of maximumDepth that was ultimately returned.
```
