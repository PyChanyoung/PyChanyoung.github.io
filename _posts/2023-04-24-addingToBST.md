---
layout: single
title: "Adding to BST(using recursion)"
categories: CodingInterview
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Definition

I'm going to implement an `add` method to insert nodes into a BST.

There is a specific feature in binary search trees where the left subtree of each node always contains values smaller than the node itself, and the right subtree contains values larger than the node.

For example, if there is a root node with the value '50', and you want to add a value smaller than the node's value, it would be added to the left subtree.

It can be solved by recursion. The reasons why using recursion are make the code conciseness and make the problem simple.

Let's see how it works with pseudo code.

## Pseudo code

First of all, we are going to get the `generic type` data on `add` method(return type void).
And we're going to check data is null. If data is null, we'll throw the `IllegalArgumentException`.

```
private void add(T data) {
    if (data == null) {
        throw new IllegalArgumentException();
    }
}
```

and in the else case, we will use a `addHelper` method to perform the recursion.

```
private void add(T data) {
    if (data == null) {
        throw new IllegalArgumentException();
    }
    root = addHelper(data, root);
}
```

In the `addHelper` method, we will receive the `data` and `node` as input. The return type of this method is the same as the type of the node.

```
private BSTNode<T> addHelper(T data, BSTNode<T> node) {

}
```
