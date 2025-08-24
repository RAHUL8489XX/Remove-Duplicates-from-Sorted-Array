# 🧹 Remove Duplicates from Sorted Array

This repo contains my solution to [LeetCode Problem 26: Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/submissions/1746117932/) — a foundational challenge that teaches in-place array manipulation using the two-pointer technique.

---
## 📊 Complexity
Time: O(n) — single pass through the array

Space: O(1) — in-place modification, no extra space
## 🧠 Problem Summary

Given a sorted array `nums`, remove the duplicates in-place so that each unique element appears only once.  
Return the number of unique elements `k`, and ensure the first `k` elements of `nums` contain the unique values.
## ✅ Approach
Since the array is sorted, duplicates are always adjacent. I used a two-pointer technique:

i tracks the position of the last unique element.

j scans through the array.

When nums[j] != nums[i], we increment i and copy nums[j] to nums[i].
### Example:
```text
Input:  nums = [1,1,2]
Output: 2, nums = [1,2,_]

Input:  nums = [0,0,1,1,1,2,2,3,3,4]
Output: 5, nums = [0,1,2,3,4,_,_,_,_,_]
