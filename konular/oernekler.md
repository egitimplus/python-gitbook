# Örnekler

```python
# Checking if list is empty

lst = []
if not lst:
    print("list is empty") # list is empty

# Checking whether an item is in a list
lst = ['test', 'twest', 'tweast', 'treast']

print('test' in lst)
# Out: True

print('toast' in lst)
# Out: False
```

```python
#  Iterating over a list

my_list = ['foo', 'bar', 'baz']
for item in my_list:
    print(item) 

'''
foo
bar
baz
'''

# You can also get the position of each item at the same time:
for (index, item) in enumerate(my_list):
    print('The item in position {} is: {}'.format(index, item))
'''
The item in position 0 is: foo
The item in position 1 is: bar
The item in position 2 is: baz
'''

# The other way of iterating a list based on the index value:
for i in range(0,len(my_list)):
    print(i, my_list[i])
'''
0 foo
1 bar
2 baz
'''
# Note that changing items in a list while iterating on it may have unexpected results:

for item in my_list:
    if item == 'foo':
        del my_list[0]
        print(item)

print(my_list) # ['bar', 'baz']
'''
foo
'''
```

```python
# For mutable elements, the same construct will result in all elements of the 
# list referring to the same object, for example, for a set:

my_list=[{1}] * 10
print(my_list) # [{1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}]

my_list[0].add(2)
print(my_list) # [{1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}]
```

```python
#  Changing Types in a List

# Convert a list of strings to integers.
items = ["1","2","3","4"]
new_list = [int(item) for item in items]
print(new_list)
# Out: [1, 2, 3, 4]

# Convert a list of strings to float.
items = ["1","2","3","4"]
new_list = map(float, items)
print(list(new_list))
# Out:[1.0, 2.0, 3.0, 4.0]

```

```python
# Shifting a list using slicing
def shift_list(array, s):
    """Shifts the elements of a list to the left or right.
    Args:
    array - the list to shift
    s - the amount to shift the list ('+': right-shift, '-': left-shift)
    Returns:
    shifted_array - the shifted list
    GoalKicker.com – Python® Notes for Professionals 145
    """
    # calculate actual shift amount (e.g., 11 --> 1 if length of the array is 5)
    s %= len(array)

    # reverse the shift direction to be more intuitive
    s *= -1
    
    # shift array with list slicing
    shifted_array = array[s:] + array[:s]
    
    return shifted_array

my_array = [1, 2, 3, 4, 5]

# negative numbers
shift_list(my_array, -7) # Out: [3, 4, 5, 1, 2]

# no shift on numbers equal to the size of the array
shift_list(my_array, 5) # Out: [1, 2, 3, 4, 5]

# works on positive numbers
shift_list(my_array, 3) # Out: [3, 4, 5, 1, 2]
```

```
# Avoid repetitive and expensive operations using conditional clause

def f(x):
    import time
    time.sleep(.1) # Simulate expensive function
    return x**2

[f(x) for x in range(1000) if f(x) > 10] # [16, 25, 36, ...]

# Instead, you should evaluate the expensive operation only once for each value 
# of x by generating an intermediate iterable (generator expression) as follows:

[v for v in (f(x) for x in range(1000)) if v > 10] # [16, 25, 36, ...]

# Or, using the builtin map equivalent:
[v for v in map(f, range(1000)) if v > 10] # [16, 25, 36, ...]

# Another way that could result in a more readable code is to put the partial 
# result (v in the previous example) in an iterable (such as a list or a tuple) 
# and then iterate over it. Since v will be the only element in the iterable, 
# the result is that we now have a reference to the output of our slow function 
# computed only once:

[v for x in range(1000) for v in [f(x)] if v > 10] # [16, 25, 36, ...]

# However, in practice, the logic of code can be more complicated and it's 
# important to keep it readable. In general, a separate generator function is 
# recommended over a complex one-liner:

def process_prime_numbers(iterable):
    for x in iterable:
        if is_prime(x):
            yield f(x)

[x for x in process_prime_numbers(range(1000)) if x > 10] # [11, 13, 17, 19, ...]


```

```
# Refactoring filter and map to list comprehensions


# Filter:
filter(lambda x: x % 2 == 0, range(10)) # even numbers < 10

# P(x) = x % 2 == 0
# S = range(10)
# filter(P, S) == [x for x in S if P(x)]

[x for x in range(10) if x % 2 == 0]

# Map
map(lambda x: 2*x, range(10)) # multiply each number by two

# F(x) = 2*x
# S = range(10)
# map(F, S) == [F(x) for x in S]

[2*x for x in range(10)]
```

```
#  Comprehensions involving tuples

[x + y for x, y in [(1, 2), (3, 4), (5, 6)]]
# Out: [3, 7, 11]

[x + y for x, y in zip([1, 3, 5], [2, 4, 6])]
# Out: [3, 7, 11]

# This is just like regular for loops:

for x, y in [(1,2), (3,4), (5,6)]:
    print(x+y)

# Note however, if the expression that begins the comprehension is a tuple then
# it must be parenthesized:

[x, y for x, y in [(1, 2), (3, 4), (5, 6)]]
# SyntaxError: invalid syntax

[(x, y) for x, y in [(1, 2), (3, 4), (5, 6)]]
# Out: [(1, 2), (3, 4), (5, 6)]

```

```
# Counting Occurrences Using Comprehension

# Count the numbers in `range(1000)` that are even and contain the digit `9`:
print (sum(
 1 for x in range(1000)
 if x % 2 == 0 and
 '9' in str(x)
))
# Out: 95
```

