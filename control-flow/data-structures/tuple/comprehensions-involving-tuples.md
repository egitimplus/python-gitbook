# Comprehensions involving tuples

```python
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
