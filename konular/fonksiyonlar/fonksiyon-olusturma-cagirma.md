---
description: Define & Call Function
---

# Fonksiyon Oluşturma / Çağırma

```
f(x) = 2x + 5

x -> 3
f(x) = 2 * 3 + 5
f(x) = 11

x -> 5
f(x) = 2 * 5 + 5
f(x) = 15
```

## fonksiyon oluşturma

Fonksiyonlar def ile tanımlanır.

```python
def fruit_juicer():
    """
    function description
    """
    print('I am fruit juicer')
```

## help()

```python
print(help(len))

'''
Help on built-in function len in module builtins:

len(obj, /)
    Return the number of items in a container.
'''
```

```python
print(help(fruit_juicer))

'''
Help on function fruit_juicer in module __main__:

fruit_juicer()
    function description
'''
```

## fonksiyon çağırma

```
print(fruit_juicer)
# <function fruit_juicer at 0x7f099253fd40>

fruit_juicer()
# I am fruit juicer
```
