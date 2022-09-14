# Tuple

```python
# a tuple is a comma-separated list of values

t = ('a', 'b', 'c', 'd', 'e')
print(type(t)) # <type 'tuple'>

# Note that a single value in parentheses is not a tuple:
t2 = ('a')
print(type(t2)) # <type 'str'>

# To create a singleton tuple it is necessary to have a trailing comma.
t2 = ('a',)
print(type(t2)) # <type 'tuple'>

# Another way to create a tuple is the built-in function tuple.
t = tuple('lupins')
print(print(t)) # ('l', 'u', 'p', 'i', 'n', 's')

# Tuples are immutable
t = (1, 4, 9)
t[0] = 2
# TypeError: 'tuple' object does not support item assignment
```
