---
description: Membership Operators
---

# Üyelik Operatörleri

| Operatör | Açıklama                                                   |
| -------- | ---------------------------------------------------------- |
| in       | Eğer nesne içerisinde aranan varsa True  döner yoksa False |
| not in   | Eğer nesne içerisinde aranan  varsa False yoksa True döner |
|          |                                                            |

```python
text = 'Hello World Again'

# küçük büyük harf duyarlıdır

print('World' in text) # True
print('world' in text) # False
print('x' not in text) # True

print(type(True)) # <class 'bool'>
print(int(True))  # 1
print(int(False)) # 0
```
