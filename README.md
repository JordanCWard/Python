# Python Practice

<!-- Hidden text for templates

/*
https://leetcode.com/problemset/
*/

/*

*/

``` python

```
<br>

-->


2. Palindrome number

Given an integer x, return true if x is a palindrome, and false otherwise.

``` python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        if x < 0:
            return False
        return x == int(str(x)[::-1])
```
<br>


1. Two sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order.

``` python
class Solution(object):
    def twoSum(self, nums, target):
        num_map = {}
        for i, num in enumerate(nums):
            complement = target - num
            if complement in num_map:
                return [num_map[complement], i]
            num_map[num] = i
```
