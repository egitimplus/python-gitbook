---
description: Global Variable
---

# Global Değişken

Global değişken fonksiyon içerisinde de çalışır

```python
if 'x' in globals():
    del x

x = 'global_variable'

def my_function():
    print('inside: ', x)

my_function()         # inside:  global_variable
print('outside: ', x) # outside:  global_variable
```
