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

## Example Prompt:
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


### With the Sliding Window method:
- Time Complexity: O(N)
- Space Complexity: O(1)
```
function findAverage(k, arr) {
  const result = [];
  let windowSum = 0;
  let windowStart = 0;

  for (let windowEnd = 0; windowEnd < arr.length; windowEnd++) {
    // add next element
    windowSum += arr[windowEnd];
   // slide window if hit required window size of 'k'
   if (windowEnd >= k - 1) {
     result.push(windowSum / k);
     // subtract element going out
     windowSum -= arr[windowStart];
     // slide window ahead
     windowStart += 1;
   }
  }
  return result;
}
```