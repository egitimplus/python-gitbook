---
description: Boolean Operators
---

# Mantıksal Operatörler



| Operatör | Açıklama                                               |
| -------- | ------------------------------------------------------ |
| and      | Eğer tüm ifadeler doğru ise True döner                 |
| or       | Eğer bir tane ifade bile doğru ise True döner          |
| not      | Sonucu ters çevirir. True -> False, False -> True olur |

```python
print(True and True)
print(True and False)
print(False and False)
print(True or True)
print(True or False)
print(False or False)
print(not True)
print(not not True)
```

```
True
False
False
True
True
False
False
True
```

```python
'''
The and operator evaluates all expressions and returns the last expression if 
all expressions evaluate to True.
Otherwise it returns the first value that evaluates to False:
'''

print(1 and 2) # 2
print(1 and 0) # 0
print(1 and "Hello World") # "Hello World"
print("" and "Pancakes") # ""

'''
The or operator evaluates the expressions left to right and returns the first value that evaluates to True or the last
value (if none are True).
'''

print(1 or 2) # 1
print(None or 1) # 1
print(0 or []) # []

'''
Lazy evaluation
When you use this approach, remember that the evaluation is lazy. Expressions that are not required to be
evaluated to determine the result are not evaluated. For example:
'''
def print_me():
    print('I am here!')

0 and print_me() # 0

```

```
2
0
Hello World

1
1
[]
0
```
