---
layout: single
title: "CocktailShakerSort"
categories: DataStructure&Algorithm
tag: [DataStructure, Algorithm, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Cocktail Shaker Sort

The Cocktail Shaker Sort, an application of the Bubble Sort algorithm, sorts an array by bubbling through it back and forth.<br>
This algorithm utilizes the Last Swap Optimization to commence the sorting process from both the far left and far right ends, successively.<br>


## Core logic code

```
boolean swapsMade = true;
int startIdx = 0;
int endIdx = arr.length -1;

while (swapsMade) {
    swapsMade = false;
    for (int i = startIdx; i < endIdx; i++) {
        if (arr[i] > arr[i+1]) {
            int temp = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = temp;
            swapsMade = true;
            endIdx = i;
        }
    }

    if (swapsMade) {
        swapsMade = false;
        for (int i = endIdx; startIdx < i; i--) {
            if (arr[i-1] > arr[i]) {
                int temp = arr[i-1];
                arr[i-1] = arr[i];
                arr[i] = temp;
                swapsMade = true;
                startIdx = i;
            }
        }
    }
}
```