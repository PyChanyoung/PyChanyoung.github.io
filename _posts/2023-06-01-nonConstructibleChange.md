---
layout: single
title: "AlgoExpert(Easy) - Non Constructible Change"
categories: CodingInterview
tag: [Python, Algorithm, Coding, Blind75]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Question

Given an array of positive integers representing the values of conis in your possession, write a function that returns the minimum amount of change (the minimum sum of money) that you **cannot** create. The given coins can have any positive integer value and aren't necessarily unique(i.e., you can have multiple coins of the same value).<br><br>
For example, if you're given coins = `[1, 2, 5]`, the minimum amount of change that you can't create is `4`. If you're given no coins, the minimum amount of change that you can't create is `1`.

**Sample Input**<br>
`coins = [5, 7, 1, 1, 2, 3, 22]`<br><br>
**Sample Output**<br>
`20`<br><br>

## Solution

예를 들어 코인이 `5` 하나만 있다고 가정할 경우, 만들 수 없는 최소한의 거스름은 `1`이 된다. `1`이 아닌 양수라면 어떤수가 들어오더라도 만들 수 없는 최소한의 값은 `1`이다. 그렇다면 만약에 `[5, 1]`이 주어진 배열이라고 하면 `1`부터 확인하는게 더 효율적일 수 있다는 이야기다. 그 말인 즉슨 정렬을 통하여 가장 작은수부터 오름차순으로 배열을 만든다음에 문제를 해결하는것을 고려해볼 수 있다는 이야기이다.

```python
def nonConstructibleChange(coins):

```
