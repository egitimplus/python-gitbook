# Demet

a tuple is a comma-separated list of values

```python
t = ('a', 'b', 'c', 'd', 'e')
type(t) # <type 'tuple'>
```

Note that a single value in parentheses is not a tuple:

```python
t2 = ('a')
type(t2) # <type 'str'>Oluşturma
```

## Oluşturma

To create a singleton tuple it is necessary to have a trailing comma.

```python
t2 = ('a',)
type(t2) # <type 'tuple'>
```

Another way to create a tuple is the built-in function tuple.

```
t = tuple('lupins')
print(t) # ('l', 'u', 'p', 'i', 'n', 's')
```

## Ekleme & Güncelleme

Tuples are immutable

```
t = (1, 4, 9)
t[0] = 2
# TypeError: 'tuple' object does not support item assignment
```

```
# Similarly, tuples don't have .append and .extend methods as list does. 
# Using += is possible, but it changes the binding of the variable, and not the tuple itself:

t = (1, 2)
q = t
t += (3, 4)
t # (1, 2, 3, 4)
q # (1, 2)

```

```python
# Index and Slicing like as Lists



```

## Packing and Unpacking&#x20;

```python
# Packing and Unpacking Tuples

# Tuples in Python are values separated by commas. Enclosing parentheses for
# inputting tuples are optional, so the two assignments

a = 1, 2, 3 # a is the tuple (1, 2, 3)
a = (1, 2, 3) # a is the tuple (1, 2, 3)

# To unpack values from a tuple and do multiple assignments use
# unpacking AKA multiple assignment

x, y, z = (1, 2, 3)
# x == 1
# y == 2
# z == 3

# The symbol _ can be used as a disposable variable name

a = 1, 2, 3, 4
_, x, y, _ = a
# x == 2
# y == 3

# To tell Python that a variable is a tuple and not a single value you can use
# a trailing comma

a = 1 # a is the value 1
a = 1, # a is the tuple (1,)

# A comma is needed also if you use parentheses

a = (1,) # a is the tuple (1,)
a = (1) # a is the value 1 and not a tuple

# Single element tuples:

x, = 1, # x is the value 1
x = 1, # x is the tuple (1,)

# * prefix can be used as a catch-all variable 

first, *more, last = (1, 2, 3, 4, 5)
# first == 1
# more == [2, 3, 4]
# last == 5
```

```python
# Comparison

'''
If elements are of the same type, python performs the comparison and returns the result. If elements are different
types, it checks whether they are numbers.
- If numbers, perform comparison.
- If either element is a number, then the other element is returned.
- Otherwise, types are sorted alphabetically .
If we reached the end of one of the lists, the longer list is "larger." If both list are same it returns 0
'''
tuple1 = ('a', 'b', 'c', 'd', 'e')
tuple2 = ('1','2','3')
tuple3 = ('a', 'b', 'c', 'd', 'e')

cmp(tuple1, tuple2)
# Out: 1

cmp(tuple2, tuple1)
# Out: -1

cmp(tuple1, tuple3)
# Out: 0

# Length

len(tuple1)
# Out: 5

# Max and Min
max(tuple1)
# Out: 'e'

min(tuple1)
# Out: 'a'

# Convert list top tuple
list = [1,2,3,4,5]
tuple(list)
# Out: (1, 2, 3, 4, 5)

# concatenation
tuple1 + tuple2
# Out: ('a', 'b', 'c', 'd', 'e', '1', '2', '3')

# hashable
hash( (1, 2) ) # ok
hash( ([], {"hello"}) # not ok, since lists and sets are not hashableyth
```

## Comprehensions

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
