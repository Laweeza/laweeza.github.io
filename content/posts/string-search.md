---
title: "String Search"
date: 2022-02-23T00:33:37-08:00
description: "An easy string technical challenge."
type: post
tags: ["string", "leetcode"]
---

## String Search

Given an array of strings and a search string as parameters, return a sorted array with these rules:
* Exact match
* Partial match
* Everything else

Account for case sensitivity and white spaces.

 ![String Search](/images/redo.png)

 ### Explanation:
 Check to see if the array has an exact match with the search string.

 If there is no exact match, check to see if the elements in the array includes the search string as a substring.


[Userful tool to check Regex](https://regex101.com/)
