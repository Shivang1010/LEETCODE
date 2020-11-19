# LEETCODE + ALGOEXPERT

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
1. Two Sum
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

#O(n^2)time O(1) space 
def twonumbersum(array, targetsum):
    for i in range(len(array)-1):
        firstnum=array[i]
        for j in range(i+1, len(array)):
            secondnum=array[j]
            if firstnum + secondnum == targetnum:
                return[firstnum, secondnum]
    return[]
#O(n) time O(n) space
def twonumbersum(array, targetsum):
    nums = {}
    for num in array:
        potentialmatch = targetsum - num
        if potentialmatch in nums:
            return[potentialmatch, num]
        else:
            nums[num] = True
    return[] 
#O(n log n) time O(1) space #space better than second solution but time worse #time complexity very uch better than 1st solution but not better than second solution
def twonumbersum(array, targetsum):
    array.sort()
    left=
    right=len(array)-1
    while left<right:
        currentsum= array[left]+array[right]
        if currentsum==targetsum:
            return[array[left],array[right]]
        elif currentsum < targetsum:
            left += 1
        elif currentsum > targetsum:
            right -= 1
    return[]
    
`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
2. Three Number Sum
#O(n^2) time O(n) space
def threenumbersum(array, targetsum):
    array.sort()
    triplets=[]
    for i in range(len(array)-2):
        left = i+1
        right= len(array)-1
        while left < right:
            currentsum= array[i] + array[left]+ array[right]
            if currentssum == targetsum:
                triplets.append([array[i],array[left],array[right]})
                left+=1
                right-=1
            elif currentsum < targetsum:
                left+=1
            elif currentsum > ttargetsum:
                right-=1
      return triplets

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

3.


`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
