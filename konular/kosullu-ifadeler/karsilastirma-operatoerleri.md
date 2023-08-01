---
description: Comparison Operators
---

# karşılaştırma operatörleri



<table><thead><tr><th width="137">Operatör</th><th width="187">Açıklama</th><th width="161">Örnek</th><th>Sonuç</th></tr></thead><tbody><tr><td>==</td><td>Eşittir</td><td>5 == 6</td><td>False</td></tr><tr><td>!=</td><td>Eşit Değildir</td><td>5 != 6</td><td>True</td></tr><tr><td>></td><td>Büyüktür</td><td>6 > 4</td><td>True</td></tr><tr><td>&#x3C;</td><td>Küçüktür</td><td>6 &#x3C; 4</td><td>False</td></tr><tr><td>>=</td><td>Büyük Eşittir</td><td>6 >= 5</td><td>True</td></tr><tr><td>&#x3C;=</td><td>Küçük Eşittir</td><td>5 &#x3C;= 4</td><td>False</td></tr></tbody></table>

```python
# Equal ( == )
# Note that == is a comparison operator, while = is an assignment operator

print(5 == 5)   # True
print(5 == '5') # False

# Not Equal ( =! )
print(3 != 4)   # True

# Greater Than ( > )
print(6 > 4)    # True

# Less Than ( < )
print(3 < 5)    # True

# Greater Than or Equal To ( >= )
print(7 >= 7)   # True

# Less Than or Equal To ( <= )
print(5 <= 7)   # True
```

## Zincirleme Koşullar

```python
# Chained

1 < 2 < 3          # True
1 < 2 and 2 < 3    # True

1 < 3 > 2          # True
1 < 3 and 3 > 2    # True
```

## is ifadesi

{% hint style="info" %}
a == b -> a ve b'nin değerlerini karşılaştırır&#x20;

a is b -> a ve b'nin kimliklerini karşılaştırır
{% endhint %}

```python
a = 'Python is fun!'
b = 'Python is fun!'

print(a == b) # True
print(a is b) # False

print(id(a)) # 2570926058312
print(id(b)) # 2570926057736
```

{% hint style="info" %}
Kısa string ve küçük tam sayılarda (256'dan küçük) performans sebebiyle aynı değere sahip değişkenlerin kimlikleri de aynıdır.
{% endhint %}

```python
a = 'short'
b = 'short'
print(a is b) # True

c = 5
d = 5
print(c is d) # True
```

{% hint style="info" %}
Uzun string ve büyük sayılarda kimlikleri aynı değildir
{% endhint %}

```python
a = 'not so short'
b = 'not so short'
print(a is b) # False

c = 1000
d = 1000
print(c is d) # False
```
