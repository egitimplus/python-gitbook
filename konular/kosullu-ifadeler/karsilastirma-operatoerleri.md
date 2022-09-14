---
description: Comparison Operators
---

# Karşılaştırma Operatörleri

| İşlem                                 | Operatör |
| ------------------------------------- | -------- |
| Eşit (Equal)                          | ==       |
| Eşit Değil (Not Equal)                | !=       |
| Büyük (Greater Than)                  | >        |
| Küçük (Less Than)                     | <        |
| Büyük Eşit (Greater Than or Equal To) | >=       |
| Küçük Eşit (Less Than Or Equal To)    | <=       |
| Aynı (Is)                             | is       |

```python
print(5 == 5)   # True
print(5 == '5') # False
print(3 != 4)   # True
print(6 > 4)    # True
print(3 < 5)    # True
print(7 >= 7)   # True
print(5 <= 7)   # True
```

<pre class="language-python"><code class="lang-python">'''
Comparison by `is` vs `==`

a == b compares the value of a and b.
a is b will compare the identities of a and b
'''

a = 'Python is fun!'
b = 'Python is fun!'
print(a == b) # True
print(a is b) # False

'''
Short strings and small
integers will return True when compared with is, due to the Python machine attempting to use less memory for
identical objects.
'''
a = 'short'
b = 'short'
c = 5
d = 5
print(a is b) # True
print(c is d) # True

'''
But longer strings and larger integers will be stored separately.
'''
a = 'not so short'
b = 'not so short'
c = 1000
d = 1000
<strong>print(a is b) # False
</strong>print(c is d) # False</code></pre>

