# Asteriks

### General Usage Of \* and \*\* <a href="#general-usage-of-and" id="general-usage-of-and"></a>

is used as multiplication operator whereas \*\* is used as a power operator.

```
## declaring variables
a, b = 2,3

## multiplication
print("Multiplication of 2 and 3 is {}".format(a * b))

## as power operator
print("2 power 3 is {}".format(a ** b))
```

## 1. Unpacking Using \* <a href="#1.-unpacking-using" id="1.-unpacking-using"></a>

```
## general approach
nums = [i for i in range(1, 6)]
a = nums[0]
b = nums[1:]
print(a, b) # 1 [2, 3, 4, 5]

## hard approach
squares = [i ** 2 for i in range(1, 6)]
a = squares[0]
b = []
for i in range(1, len(squares)):
    b.append(squares[i])
print(a, b) # 1 [4, 9, 16, 25]

nums = [i for i in range(1, 6)]

## a will be 1 and b will be a list containing remaining elements
a, *b = nums
print(a, b) # 1 [2, 3, 4, 5]

## using tuple
## here first element will assign to a and last element to c
a, *b, c = (1, 2, 3, 4, 5)
print(a, b, c) # 1 [2, 3, 4] 5

## using sets
a, *b, c = {1, 4, 9, 16, 25}
print(a, b, c) # 1 [4, 9, 16] 25

```

### 1.1. Combining Different Iterables <a href="#1.1.-combining-different-iterables" id="1.1.-combining-different-iterables"></a>

```
## combining a tuple, list, set
nums = [1, 2, 3]
nums2 = (4, 5, 6)
nums3 = {7, 8, 9}

_list = [*nums, *nums2, *nums3]    # [1, 2, 3, 4, 5, 6, 8, 9, 7]
_tuple = (*nums, *nums2, *nums3)   # (1, 2, 3, 4, 5, 6, 8, 9, 7) 
_set = {*nums, *nums2, *nums3}     # {1, 2, 3, 4, 5, 6, 7, 8, 9}
```

### 1.2. Nested Unpacking

```
languages = ["Python", "HTML", "CSS", "JS"]

## unpacking
[[first_letter, *remaining], *other] = languages

print(first_letter, remaining, other) # P ['y', 't', 'h', 'o', 'n'] ['HTML', 'CSS', 'JS']
```



1. \


\
