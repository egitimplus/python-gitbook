# Asteriks

### General Usage Of \* and \*\* <a href="#general-usage-of-and" id="general-usage-of-and"></a>

is used as multiplication operator whereas \*\* is used as a power operator.

```python
## declaring variables
a, b = 2,3

## multiplicationPyt
print("Multiplication of 2 and 3 is {}".format(a * b))

## as power operator
print("2 power 3 is {}".format(a ** b))
```

## 1. Unpacking Using \* <a href="#1.-unpacking-using" id="1.-unpacking-using"></a>

```python
## general approach
nums = [1, 2, 3, 4, 5]
a = nums[0]
b = nums[1:]
print(a, b) # 1 [2, 3, 4, 5]

## hard approach
squares = [1, 4, 9, 16, 25]
a = squares[0]
b = []
for i in range(1, len(squares)):
    b.append(squares[i])
print(a, b) # 1 [4, 9, 16, 25]

nums = [1, 2, 3, 4, 5)]

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

```python
## combining a tuple, list, set
nums = [1, 2, 3]
nums2 = (4, 5, 6)
nums3 = {7, 8, 9}

_list = [*nums, *nums2, *nums3]    # [1, 2, 3, 4, 5, 6, 8, 9, 7]
_tuple = (*nums, *nums2, *nums3)   # (1, 2, 3, 4, 5, 6, 8, 9, 7) 
_set = {*nums, *nums2, *nums3}     # {1, 2, 3, 4, 5, 6, 7, 8, 9}
```

### 1.2. Nested Unpacking

```python
languages = ["Python", "HTML", "CSS", "JS"]

## unpacking
[[first_letter, *remaining], *other] = languages

print(first_letter, remaining, other) # P ['y', 't', 'h', 'o', 'n'] ['HTML', 'CSS', 'JS']
```

## 2. Unpacking Using \*\*

```python
## sample dictionary
person = {"name":"John", "age":19, "year_of_passing":"2021"}
string = "Name:-{name} Year Of Graduation:-{year_of_passing} Age:-{age}".format(**person)
print(string) # Name:-John Year Of Graduation:-2021 Age:-19

```

## 3. Asterisks in Functions <a href="#3.-asterisks-in-functions" id="3.-asterisks-in-functions"></a>

### 3.1. Unpacking in Functions <a href="#3.1.-unpacking-in-functions" id="3.1.-unpacking-in-functions"></a>

```python
nums = [1, 2, 3, 4, 5]
## passsing list using the *
print(*nums) # 1 2 3 4 5
```

### 3.2. Packing Elements <a href="#3.2.-packing-elements" id="3.2.-packing-elements"></a>

```python
def average(*nums):
    return sum(nums) / len(nums)
    
print(average(1, 2, 3, 4, 5)) # 3.0

```

```python
def _object(name, **properties):
    print(name, properties)

_object("Car", color="Red", cost=999999, company="Ferrari")

# Car {'ceo': 'Louis', 'color': 'Red', 'cost': 999999, 'company': 'Ferrari'}
```

## 4. Keyword-Only Arguments with Positional Arguments <a href="#4.-keyword-only-arguments-with-positional-arguments" id="4.-keyword-only-arguments-with-positional-arguments"></a>

```python
def keyword_only(*items, _list, default = False):
    print(items)
    print(_list)
    print(default)
    
nums = [1, 4, 9, 16, 25]
## calling the function
keyword_only(1, 2, 3, 4, 5, _list = nums, default = True)

'''
(1, 2, 3, 4, 5)
[1, 4, 9, 16, 25]
True
'''

nums = [i ** 2 for i in range(1, 6)]
## calling the function will raise an error
keyword_only(1, 2, 3, 4, 5, nums, False) # TypeError: keyword_only() missing 1 required keyword-only argument: '_list'
```



## 5. Keyword-Only Arguments without Positional Arguments

```python
def _sample(*, name):
    print(name)
    
## calling the function using keyword 'name'
_sample(name = "Datacamp") # Datacamp

## calling the function without using keyword 'name'
## we will get a TypeError
_sample("Datacamp") # TypeError: samp() takes 0 positional arguments but 1 was given

```

\


\


\


\
\
