---
description: Boolean Operators
---

# Mantıksal Operatörler

## and

Tüm ifadeleri çalıştırır hepsi True ise sondaki ifadeyi döndürür eğer False varsa ilk False değeri dönderir.

```python
print(True and True)    # True
print(True and False)   # False
print(False and False)  # False

print(1 and 2) # 2
print(1 and 0) # 0
print(1 and "Hello World") # "Hello World"
print("" and "Pancakes") # ""
print(" " and "Pancakes") # Pancakes
print(None and "Pancakes") # None
```

## or

Soldan sağa doğru ifadeleri sırayla çalıştırır ve ilk bulduğu True değeri dönderir. Eğer hiç True yoksa son değeri dönderir.

```python
print(True or True)     # True
print(True or False)    # True
print(False or False)   # False

print(1 or 2) # 1
print(None or 1) # 1
print(0 or []) # []

```

## not

Sonucu ters çevirir. True -> False, False -> True olur

```python
print(not True)         # False
print(not not True)     # True
```

## lazy evaluation

Sonucu belirlemek için değerlendirilmesi gerekmeyen ifadeler değerlendirilmez.

```python
0 and print('Hello World') # 0
```

```python
def true_func():
    print("true_func()")
    return True

def false_func():
    print("false_func()")
    return False

print(true_func() or false_func())
# true_func()
# True

print(false_func() or true_func())
# false_func()
# true_func()
# True

print(true_func() and false_func())
# true_func()
# false_func()
# False

print(false_func() and false_func())
# false_func()
# False
```

## bool()

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
print(bool('Emre')) # True
```

## tam sayıya çevirme

```python
print(int(True))  # 1
print(int(False)) # 0
```
