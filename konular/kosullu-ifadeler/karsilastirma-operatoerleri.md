---
description: Comparison Operators
---

# Karşılaştırma Operatörleri

| İşlem      | Operatör |
| ---------- | -------- |
| Eşit       | ==       |
| Eşit Değil | !=       |
| Büyük      | >        |
| Küçük      | <        |
| Büyük Eşit | >=       |
| Küçük Eşit | <=       |
| Aynı       | is       |

```python
print(5 == 5) # Equal
print(5 == '5') # Equal
print(3 != 4) # Not Equal
print(6 > 4) # Greater Than
print(3 < 5) # Less Than
print(7 >= 7) # Greater Than or Equal To
print(5 <= 7) # Less Than Or Equal To
```

```
True
False
True
True
True
True
True
```

<pre class="language-python"><code class="lang-python">'''
Comparison by `is` vs `==`

a == b compares the value of a and b.
a is b will compare the identities of a and b
'''

a = 'Python is fun!'
b = 'Python is fun!'
print(a == b) # returns True
print(a is b) # returns False

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

```
True
False
True
True
False
False
```

