---
title: Practice Arrays with Python Code
author: Maged Helmy
date: 2019-09-01 14:00:00 +0100
categories: [Blogging, Computer Science]
tags: [arrays]
---

485: Max Consecutive Ones: Given a binary array, find the maximum number of consecutive 1s in this array.
Explanation: We create two variables, one called counter which keeps track of the number of 1's it encounters and max_consecutive which keeps track of the number of consective 1's it meet if there is a zero in the middle. With an if loop, if 1 is encountered you increment the counter, and update the value of max_consecutive, else you zero the counter. You do a final max() check both on the counter and max_consecutive on the return loop just in case the last value was not 1.

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
Explanation: We need to first create 3 variables. The first variable keeps count of the total number of even numbers in the list. Then two more variables, one to keep count of the length of the individual elements in the list, and one to actually count the length of the values. We iterate through the list, element by element, and count the number of values in the list by using the modules and division method, i.e: ```              value = value * 10 + num % 10  and num = num // 10 ```, and adding a while loop and counter, to keep track of how long this operation goes. This value is then checked if it is even by using this modulus ```  counter % 2 == 0:``` and iterating on the counter if it is.

```Python
class Solution:
    def findNumbers(self, nums: List[int]) -> int:
        count= 0

        for num in nums:
            value = 0
            counter = 0

            while num != 0:
                value = value * 10 + num % 10
                num = num // 10
                counter += 1

            if counter % 2 == 0:
                count+=1

        return count
```
--------------------------
