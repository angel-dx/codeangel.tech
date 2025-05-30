---
title: "Leetcod 217: Contains Duplicate"
date: 2024-09-29
tags: ["DSA", "Data Structure", "Algorithms", "Note", "Arrays", "Hashmap", "leetcode", "neetcode"]
images: [
    "/images/notes/leetcode-217-contains-duplicate/leetcode-217-contains-duplicate.jpg"
]
draft: false
---

## Problem

LeetCode 217 - Contains Duplicate

## Solution

Use a hash map to keep track of seen numbers. Iterate through the array once, checking if each number is already in the map. If it is, return true (duplicate found). If not, add the number to the map. If we finish iterating without finding a duplicate, return false.

## Analysis
Time Complexity: O(n) Space Complexity: O(n)


## Code
```go
package arrayshashing

func ContainsDuplicate(nums []int) bool {
	result := make(map[int]bool)
	for _, v := range nums {
		if _, exists := result[v]; exists {
			return true
		}
		result[v] = true
	}
	return false
}
```

