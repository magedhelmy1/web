---
title: Practice Arrays with Python Code
author: Maged Helmy
date: 2019-09-01 14:00:00 +0100
categories: [Blogging, Computer Science]
tags: [arrays]
---

485: Max Consecutive Ones: Given a binary array, find the maximum number of consecutive 1s in this array.
Explanation: We create two variables, one called counter which keeps track of the number of 1's it encounters and max_consecutive which keeps track of the number of consective 1's it meet if there is a zero in the middle. With an if loop, if 1 is encountered you increment the counter, and update the value of max_consecutive, else you zero the counter. You do a final max() check both on the counter and max_consecutive on the return loop just in case the last value was not 1.
--------------------------
```Python
class Solution:
    def findMaxConsecutiveOnes(self, nums: List[int]) -> int:
        max_consecutive=0
        counter= 0
        for num in nums:
            if num == 1:
                counter+=1
                max_consecutive= max(counter,max_consecutive)
            else:
                counter = 0
        return max(counter,max_consecutive)

```
--------------------------



1295: Given an array nums of integers, return how many of them contain an even number of digits.
Explanation:
--------------------------
```Python


```
--------------------------
