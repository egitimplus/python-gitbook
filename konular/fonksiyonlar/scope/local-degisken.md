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

my_function()            # inside:  local variable
print('outside: ', x)    # NameError: name 'x' is not defined
```
