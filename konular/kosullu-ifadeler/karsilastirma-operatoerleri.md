---
description: Comparison Operators
---

# Karşılaştırma Operatörleri

{% tabs %}
{% tab title="Eşit " %}
{% hint style="info" %}
Equal ( == )
{% endhint %}

```python
print(5 == 5)   # True
print(5 == '5') # False
```
{% endtab %}

{% tab title="Eşit Değil " %}
{% hint style="info" %}
&#x20;Not Equal ( =! )
{% endhint %}

```python
print(3 != 4)   # True
```
{% endtab %}

{% tab title="Büyük " %}
{% hint style="info" %}
Greater Than ( > )
{% endhint %}

```python
print(6 > 4)    # True
```
{% endtab %}

{% tab title="Küçük " %}
{% hint style="info" %}
Less Than ( < )
{% endhint %}

```python
print(3 < 5)    # True
```
{% endtab %}

{% tab title="Büyük Eşit" %}
{% hint style="info" %}
Greater Than or Equal To ( >= )
{% endhint %}

```python
print(7 >= 7)   # True
```
{% endtab %}

{% tab title="Küçük Eşit" %}
{% hint style="info" %}
Less Than or Equal To ( <= )
{% endhint %}

```python
print(5 <= 7)   # True
```
{% endtab %}

{% tab title="Aynı" %}
{% hint style="info" %}
Is ( is)

```
a == b -> a ve b'nin değerlerini karşılaştırır
a is b -> a ve b'nin kimliklerini karşılaştırır
```
{% endhint %}

```python
a = 'Python is fun!'
b = 'Python is fun!'

print(a == b) # True
print(a is b) # False

print(id(a)) # 2570926058312
print(id(b)) # 2570926057736
```

{% hint style="warning" %}
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

{% hint style="warning" %}
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
{% endtab %}
{% endtabs %}

