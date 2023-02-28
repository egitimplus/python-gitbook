# fonksiyon tanımlama

```
f(x) = 2x + 5

x -> 3
f(x) = 2 * 3 + 5
f(x) = 11

x -> 5
f(x) = 2 * 5 + 5
f(x) = 15
```

Fonksiyonlar def ile tanımlanır.

```python
def fruit_juicer():
    """
    function description : docstring
    """
    print('I am fruit juicer')
```

## Fonksiyon Yardımı - help()

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

```python
"""This is the module docstring."""

def say_hi():
    """This is the function docstring."""
    print('Hi')
    
print(func.__doc__)
print(help(func))
```

## Fonksiyon Çağırma

```python
print(fruit_juicer)
# <function fruit_juicer at 0x7f099253fd40>

fruit_juicer()
# I am fruit juicer// Some code
```
