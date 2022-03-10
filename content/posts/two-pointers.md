---
title: "Two Pointers"
date: 2022-03-09T00:48:37-10:00
description: "Core Patterns"
type: post
series:
  - coding patterns
tags: ["two pointers", "coding patterns", "sliding window", "array"]
---

A common pattern found in problems dealing with an array or a linkedlist involves finding or calculating something among subarrays or sublists of a certain size.

Given an array, find the average of all subarrays of 'K' contiguous elements in it.

An input of `[1, 3, 2, 6, -1, 4, 1, 8, 2]` & `k = 5` would yield an output of:

`[2.2, 2.8, 2.4, 3.6, 2.8]`

### With the brute force method:
- Time Complexity: O(N^2)
- Space Complexity: O(1)
```
 function findAverage(k, arr) {
   const result = [];
   for (let i = 0; i < arr.length - k + 1; i++) {
     //find sum of next 'k' elements
     let sum = 0;
     for (let j = i; j < i + k; j++) {
       sum += arr[j];
     }
     result.push(sum / k);
   }
   return result;
 }
```
