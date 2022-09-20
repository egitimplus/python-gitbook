# Return

Fonksiyonlar geriye değer döndürebilir.

```python
def fruit_juicer(fruit):
    return f'I am {fruit} juicer'

juicer = fruit_juicer('apple')
print(juicer) # I am apple juicer
```

```python
def sum(a, b):
    return a + b

result = sum(3, 5)

print(result) # 8
```

```python
def sum_minus(a, b):
    minus = a - b
    sum = a + b
    return sum, minus

result = sum_minus(3, 5)
print(result) # (8, -2)

sum, min = sum_minus(6, 2) 
print(sum, min) # 8 4
```

```python
def function(number):
    if number > 5:
        return True
    else:
        return False

print(function(3)) # False
```

```python
def function(number):
    if number > 5:
        return True
    
    return False

print(function(3)) # False
```

```python
def function(number):   
    return number > 5

print(function(3)) # False
```
