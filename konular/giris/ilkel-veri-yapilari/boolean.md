# Boolean

```python
print(type(True)) # <class 'bool'>
print(type(False)) # <class 'bool'> 
```

```python
# Returns False as x is not equal to y
print(bool(5==10)) # False
 
# Returns False as x is None
print(bool(None)) # False
 
# Returns False as x is an empty sequence
print(bool(())) # False
 
# Returns False as x is an empty mapping ("", [])
print(bool({})) # False
 
# Returns False as x is 0
print(bool(0.0)) # False
 
# Returns True as x is a non empty string
print(bool('GeeksforGeeks')) # False
```
