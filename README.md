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
            elif currentsum > targetsum:
                right-=1
      return triplets

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

3.Smallest Difference
(you are given two array of integer value and you have to find the pair of number where one number come from first array and second number come from second array and with the smallest difference in other word  find  the two closest number from both of these arrays)


#O(nlog(n) + mlog(m)) time  and O(1) space
def smallestdifference(arrayone, arraytwo):
    arrayone.sort()#in interview ask the interviewer if you can sort or not
    arraytwo.sort()#if you don't sort it will be reflected in space complexitty  if we didnt sort then there would be more space
    idxone=0
    idxtwo=0
    smallest=float("inf")    #constant space
    current= float("inf")    #constant space
    smallestpair=[]  #constant space
    while idxone<len(arrayone) and idxtwo < len(arraytwo):
        firstnum=arrayone[idxone]
        secondnum=arraytwo[idxtwo]
        #you could have also done 
        #current= abs(firstnum - secondnum)
        if firstnum < secondnum:
            current = secondnum - firstnum #then you can take out this line
            idxone+=1
        elif secondnum < firstnum:
            currentnum = firstnum - secondnum # and this line will be out but we use this so its more readable
            idxtwo +=1
        else:
            return[firstnum, secondnum]
        if smallest >current:
            smallest = current
            smallestpair=[firstnum, secondnum]
    return smallestpair


`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

4. Moving Element to end


`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````

`````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````````
