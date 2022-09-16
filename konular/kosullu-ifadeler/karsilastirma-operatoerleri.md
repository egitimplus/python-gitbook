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
{% endhint %}

```python
'''
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
print(a is b) # False
print(c is d) # Falsepy
```
{% endtab %}
{% endtabs %}

```python
```

