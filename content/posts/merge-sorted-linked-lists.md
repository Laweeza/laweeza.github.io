---
title: 'Merge Two Sorted Lists'
date: 2023-09-11T00:33:37-21:10
description: 'Easy Difficulty Leetcode Linked List Problem.'
type: post
tags: ['linked list', 'sort']
---

## Merge Two Sorted Lists:

You are given the heads of two sorted linked lists `list1` and `list2`:

Merge the two lists into one sorted list. The list should be made by splicing together the nodes of the first two lists.

Return the head of of the merged linked list.

```
/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} list1
 * @param {ListNode} list2
 * @return {ListNode}
 */
var mergeTwoLists = function(list1, list2) {
   let newList = new ListNode(0)
   let headOfList = newList;

   while(list1 !== null && list2 !== null) {
       if (list1.val < list2.val) {
           newList.next = list1;
           list1 = list1.next;
       } else {
           newList.next = list2;
           list2 = list2.next;
       }

       newList = newList.next;
   }
   if (list1 === null) {
       newList.next = list2;
   }

   if (list2 === null) {
       newList.next = list1;
   }
   return headOfList.next;
};
```

### Explanation:

Initialize a new LinkedList with a dummy ListNode.

Maintain a reference to the head of the new LinkedList.

Whilst both of the passed in lists contain more elements

If list1's value is smaller, add list1's value to the new list

Move list1 to its next element

Add list2's value to the new list

Move list2 to its next element

Move into the next level of the LinkedList for the next iteration

If list1 has run out of elements, append list1 to the new list

[Leetcode #21 Explanation](https://duncan-mcardle.medium.com/leetcode-problem-21-merge-two-sorted-lists-javascript-b5a4de3da319)
