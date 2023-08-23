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

Given the `root` of a binary tree, invert the tree, and return _its root._

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

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        // if input is Null,
        if root is None:
            // just return.
            return root

        // Assign root to `current` variable. If the value at the root is used, there is a risk of losing data in the middle of the computation.
        current = root

        // Swap left and right
        current.left, current.right = current.right, current.left

        // Left recursion
        self.invertTree(current.left)

        // Right recursion
        self.invertTree(current.right)

        // Return the value of the final transformed tree at the root.
        return root
```
