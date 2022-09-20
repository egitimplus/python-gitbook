---
description: Comparison Operators
---

# Karşılaştırma Operatörleri

| Operatör | Açıklama      | Örnek  | Sonuç |
| -------- | ------------- | ------ | ----- |
| ==       | Eşittir       | 5 == 6 | False |
| !=       | Eşit Değildir | 5 != 6 | True  |
| >        | Büyüktür      | 6 > 4  | True  |
| <        | Küçüktür      | 6 < 4  | False |
| >=       | Büyük Eşittir | 6 >= 5 | True  |
| <=       | Küçük Eşittir | 5 <= 4 | False |

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
