---
description: Local Variable
---

# Local Değişken

```python
if 'x' in globals():
    del x

def my_function():
    x = 'local variable'
    print('inside: ', x)

my_function()
print('outside: ', x)
```

```
inside:  local variable
NameError: name 'x' is not defined
```
