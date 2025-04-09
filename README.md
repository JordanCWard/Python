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


3. Roman to integer

Given a roman numeral up to 3999, convert it to an integer.

``` python
class Solution:
    def romanToInt(self, s: str) -> int:
        r_n = {
            'I': 1, 'IV': 4, 'V': 5, 'IX': 9,
            'X': 10, 'XL': 40, 'L': 50, 'XC': 90,
            'C': 100, 'CD': 400, 'D': 500, 'CM': 900,
            'M': 1000
        }

        total, i = 0, 0

        while i < len(s):
            two_digit = s[i:i+2]
            if i + 1 < len(s) and two_digit in r_n:
                total += r_n[two_digit]
                i += 2
            else:
                total += r_n[s[i]]
                i += 1
        return total
```
<br>


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
