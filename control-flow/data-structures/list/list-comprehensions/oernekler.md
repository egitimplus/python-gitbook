# Örnekler

```
numbers = []
for x in range(10):
    if x % 2 == 0:
        temp = x
    else:
        temp = -1
 
    numbers.append(2 * temp + 1)

print(numbers)
# Out: [1, -1, 5, -1, 9, -1, 13, -1, 17, -1]

# The above code is equivalent to:

[2 * (x if x % 2 == 0 else -1) + 1 for x in range(10)]
```

```
# One can combine ternary expressions and if conditions. The ternary operator works on the filtered result:

[x if x > 2 else '*' for x in range(10) if x % 2 == 0]
# Out: ['*', '*', 4, 6, 8]

# The same couldn't have been achieved just by ternary operator only:
[x if (x > 2 and x % 2 == 0) else '*' for x in range(10)]
# Out:['*', '*', '*', '*', 4, '*', 6, '*', 8, '*']

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
