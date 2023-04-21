---
layout: single
title: "Blind75 - Invert Binary Tree"
categories: CodingInterview
tag: [Python, Algorithm, Coding, Blind75]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given the `root` of a binary tree, invert the tree, and return *its root.*

<**Example 1**>
```
         4                4
       /   \            /   \
      2     7    =>    7     2
     / \   / \        / \   / \
    1   3 6   9      9   6 3   1

Input: root = [4, 2, 7, 1, 3, 6, 9]
Output: [4, 7, 2, 9, 6, 3, 1]
```

<**Example 2**>
```
         2                2
       /   \     =>     /   \
      2     7          7     2

Input: root = [2, 1, 3]
Output: [2, 3, 1]
```

<**Example 3**>
```
Input: root = []
Output: []
```

<**Constraints**>
- The number of nodes in the list is the range `[0, 100]`.
- `-100 <= Node.val <= 100`


## Solution
When we face the problem, we should think about input.
The input examples mentioned above are very balanced.
But, there can also be unbalanced inputs, such as in the case of a Degenerate tree.


```
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        // Base Case = When reach the leaf node, just return.
        if root is None:
            return

        // Using current(pointer) to reference the root node, we avoid modifying the original tree's root node.
        current = root

        // Swap current's left node and right node.
        current.left, current.right = current.right, current.left

        // Use recursion. Because node has many end points.
        self.invertTree(current.left)
        self.invertTree(current.right)
        return root
```