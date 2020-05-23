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
Question:Squares of a Sorted Array: Given an array of integers A sorted in non-decreasing order, return an array of the squares of each number, also in sorted non-decreasing order.

Explanation: We need to create three variables, an empty list, left which starts at the begining of the list, and right that starts at the end of the list. The first "while" checks that the "left" does not cross the "right" since you do not want to sort already sorted values. If the A[left] is bigger than the A[right], then square that value and append it, otherwise, append the right value. This is basically sorting while squaring at the same time.

```Python
class Solution:
    def sortedSquares(self, A: List[int]) -> List[int]:
        left = 0
        right = len(A) - 1
        result = []

        while left <= right:

            if abs(A[left]) >= abs(A[right]):
                result.append(A[left]*A[left])
                left += 1

            else:
                result.append(A[right]*A[right])
                right -= 1      

        return result[::-1]
```
--------------------------

Question: Duplicate Zeros Given a fixed length array arr of integers, duplicate each occurrence of zero, shifting the remaining elements to the right. Note that elements beyond the length of the original array are not written. Do the above modifications to the input array in place, do not return anything from your function.

Explanation: we create two variables, the length of the array to keep track when we have reached the end, and the second variable "enumerate" to get the index and value, and also to enumerate twice if the value is not the last. We use arr.insert and arr.pop, to insert zeros where needed and to drop out the last element in the array.

```Python
class Solution:
    def duplicateZeros(self, arr: List[int]) -> None:
        """
        Do not return anything, modify arr in-place instead.
        """

        arr_length= len(arr)-1
        enumerate_val= enumerate(arr)

        for i,x in enumerate_val:
            if arr[i] == 0:

                arr.insert(i+1,0)
                arr.pop()
                if i != arr_length:
                    next(enumerate_val)

```
--------------------------

Question: Merge Sorted Array Given two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.
The number of elements initialized in nums1 and nums2 are m and n respectively.
You may assume that nums1 has enough space (size that is greater or equal to m + n) to hold additional elements from nums2.

Explanation: we will fill out nums2 from the end to the begining since we have to merge nums 2 into nums 1. iterating from the beginning of nums1 list will cause alot of index shift and complications. Therefore, it is best to start iterating from the end of the list. we create 3 variables, one to keep up with the first list, one to keep up with the second list and the third to keep up with points of insertion into the first list and to merge the rest of list 2 if list 1 was shorter. We compare values from the end of list 1 with list 2. And insert whichever is bigger towards the end. Since we need to fill the list anyways. We decrement the pointer as we go along. If list 1 is exhausted before list 2, this means list 1 is shorter, therefore, we copy the rest of list 2 into list 1.

```Python
class Solution:
    def merge(self, nums1: List[int], m: int, nums2: List[int], n:int) -> None:
        list_1 = m - 1
        list_2 = n - 1
        k = m + n - 1

        while list_1 >= 0 and list_2 >= 0:

            if nums1[list_1] >= nums2[list_2]:
                nums1[k] = nums1[list_1]
                list_1 -=1

            else:
                nums1[k] = nums2[list_2]
                list_2 -=1


            k -= 1

        if list_1 < 0:
            nums1[:k+1] = nums2[:list_2+1]
```
--------------------------
Question: Remove Element: Given an array nums and a value val, remove all instances of that value in-place and return the new length. Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory. The order of elements can be changed. It doesn't matter what you leave beyond the new length.

Explanation: you need to create a new variable in this case called "j" which keeps track of the last position where "val" was not seen. If the val does not match the current item in the list then you overwrite it, and iterate. We are basically creating a counter for the number of times something has been overwritten on the list. We iterate the length of the list, and when the "val" does not match the current item in the list, we overwrite. Since its matching we will skip the value and overwrite it later.

```Python
class Solution:
    def removeElement(self, nums:List[int], val:int) -> int:

        j=0
        for i in range(len(nums)):
            if val != nums[i]:
                nums[j] =nums[i]
                j += 1

        return j

```
--------------------------
Question:Remove Duplicates from Sorted Array: Given a sorted array nums, remove the duplicates in-place such that each element appear only once and return the new length. Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

Explanation: We need to  3 variables to keep track of the array. j, keeps track of the last non-duplicate value, "i" and "i-1" looks at comparing both values in the list. We add a condition of "i==0" because the first value will always stay since the first value is always unique.

```Python
class Solution:
    def removeDuplicates_1(self, nums:List[int]) -> int:

        j = 1
        for i in range(1, len(nums)):
            if nums[i] != nums[i-1]:
                nums[j] = nums[i]
                j += 1

        return nums[:j]

      def removeDuplicates_2(self, nums:List[int]) -> int:

          j = 0
          for i in range(len(nums)):
              if nums[i] != nums[i-1] or i==0:
                  nums[j] = nums[i]
                  j += 1

          return j

```
--------------------------
Question:Check If N and Its Double Exist: Given an array arr of integers, check if there exists two integers N and M such that N is the double of M ( i.e. N = 2 * M).

Explanation:

```Python
class Solution:
    def checkIfExist(self, arr:List[int]) -> True:

        for i in range(len(arr)):
            if arr[i]*2 in arr and arr.index(arr[i]*2 ) != i:
                return True

        return False


```
--------------------------
Question: Valid Mountain Array: Given an array A of integers, return true if and only if it is a valid mountain array.

Explanation: we divide the code in three sections, going up the mountian, checking that going up has not exhausted all the steps and that the first value is not higher than the next value, and going down the mountain. The total amount of steps going up the mountain and down the mountain should be the length of the array. We create a while loop in order to iterate over all the positive values which are going up the mountain, then we check that we have actually iterated and that we have not exhausted all our steps going up, then we make there is atleast one step going down. The total of going up and down should equal the array of the list.

```Python
class Solution:
    def validMountainArray(self, A:List[int]) -> bool:

        N = len(A) - 1
        i = 0

        # going up
        while i + 1 <= N and A[i] < A[i+1]:
            i += 1

        # checking you have not exhausted the steps
        if i == 0 or i == N:
            return False

        # coming down the mountain
        while i + 1 <= N and A[i] > A[i+1]:
            i += 1

        # making sure the total of going up the mountain and coming down the mountain is equal to total amount if steps.
        return i == N

```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
Question:
Explanation:

```Python


```
--------------------------
