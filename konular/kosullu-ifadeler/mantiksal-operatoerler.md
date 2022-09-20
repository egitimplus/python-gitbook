---
description: Boolean Operators
---

# Mantıksal Operatörler

{% tabs %}
{% tab title="and" %}
{% hint style="info" %}
Tüm ifadeleri çalıştırır hepsi True ise sondaki ifadeyi döndürür eğer False varsa ilk False değeri dönderir.
{% endhint %}

```python
print(True and True)    # True
print(True and False)   # False
print(False and False)  # False

print(1 and 2) # 2
print(1 and 0) # 0
print(1 and "Hello World") # "Hello World"
print("" and "Pancakes") # ""
print(" " and "Pancakes") # Pancakes
print(None and "Pancakes") # None
```
{% endtab %}

{% tab title="or" %}
{% hint style="info" %}
Soldan sağa doğru ifadeleri sırayla çalıştırır ve ilk bulduğu True değeri dönderir. Eğer hiç True yoksa son değeri dönderir.
{% endhint %}

```python
print(True or True)     # True
print(True or False)    # True
print(False or False)   # False

print(1 or 2) # 1
print(None or 1) # 1
print(0 or []) # []

```
{% endtab %}

{% tab title="not" %}
{% hint style="info" %}
Sonucu ters çevirir. True -> False, False -> True olur
{% endhint %}

```python
print(not True)         # False
print(not not True)     # True
```
{% endtab %}

{% tab title="lazy eveluation" %}
{% hint style="info" %}
Sonucu belirlemek için değerlendirilmesi gerekmeyen ifadeler değerlendirilmez.
{% endhint %}

```python
def print_me():
    print('I am here!')

0 and print('Hello World') # 0
```
{% endtab %}
{% endtabs %}
