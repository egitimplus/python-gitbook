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

print('World' in text)
print('world' in text)
print('x' not in text)

print(type(True))
print(int(True))
print(int(False))
```

<pre><code><strong>Output:
</strong>----------------------------------------
True
False
True
&#x3C;class 'bool'>
1
0</code></pre>
