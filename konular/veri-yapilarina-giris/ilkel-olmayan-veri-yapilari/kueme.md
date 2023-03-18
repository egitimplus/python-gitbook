---
description: >-
  Sıralanamaz (not ordered), Değiştirilebilir (mutable), Tekrarlanamaz (not
  duplicate)
---

# küme

```python
x = set()
print(type(x)) # <class 'set'>

# Elemanı olan küme oluşturma
x = {1, 2, 3, 3, 4}
print(x) # {1, 2, 3, 4}

# Listeyi kümeye çevirme
list1 = [1,2,2,3,4,5,6,6,6]
print(set(list1)) # {1,2,3,4,5,6}
```
