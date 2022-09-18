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

my_function()
print('outside: ', x)
```

```
inside:  global_variable
outside:  global_variable
```
