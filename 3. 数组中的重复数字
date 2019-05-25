# offer-exercises
剑指offer 题目，python实现
#1，找出并输出数组中重复的数字，长度为n的数组的所有数字都在0到n之间
#排序实现，遍历n次，排序时间长O(nlogn)
test1 = [1,2,3,7,3,7,8,1,1]
test2 = [1,2,3]
test3 = []
def search(nums):
    if len(nums) < 2: print('No number is expected')
    nums.sort()
    i,res = 0,[]
    while i < len(nums)-1:
        if nums[i]==nums[i+1] and nums[i] not in res:
            res.append(nums[i])
        i += 1
    return res
print(search(test1))
#hash表实现，字典实现。需要额外的空间O(n)储存字典
def search2(nums):
    if len(nums) < 2: print('No number is expected')
    dirc,result = {},[]
    for i in range(len(nums)):
        if nums[i] in dirc and nums[i] not in result:
            result.append(nums[i])
        else:
            dirc[nums[i]] = 1
    return result
print(search2(test1))
#3，交换元素实现，前提是数字必须在0到n之间，空间消耗少，遍历时间为O(n)
def search3(nums):
    if len(nums) < 2: print('No number is expected')
    for i in range(len(nums)):
        if nums[i] < 0 or nums[i] > len(nums):
            return False
    count = 0
    for i in range(len(nums)):
        while nums[i]!= i and count < 3:
            count += 1
            if nums[i] == nums[nums[i]]:
                return nums[i]
            nums[i],nums[nums[i]] = nums[nums[i]],nums[i]
    return False
print(search3(test1))
print(search3(test2))
print(search3(test3))
