---
description: Variables
---

# Değişkenler

{% hint style="info" %}
değişken oluşturma
{% endhint %}

```python
x = 5       
y = "John"  

print(x) # 5
print(y) # John
```

{% hint style="info" %}
değişken tanımlama kuralları

* Harf veya alt çizgi ( \_ ) ile başlamalıdır.
* Harf, alt çizgi ( \_ ) ve rakamlardan oluşabilir.
* Kelimeler arasında boşluk bırakılamaz.
* Python tarafından ayrılmış kelimeler (reserved words) kullanılamaz.
{% endhint %}

```python
# import keyword
# print(keyword.kwlist)
class = '12-A'

# Büyük / küçük harf duyarlıdır.
Hello = 'Hello'
print(hello) # NameError: name 'hello' is not defined

# Türkçe karakterler kullanılabilir ancak kullanılmaması daha iyi olacaktır
adı = 'Emre'
print(adı) # Emre

# İsimlendirme yaparken değişken isimlerini tamamen küçük harfle ve aralarında 
# alt çizgi (snake case) kullanılması tavsiye edilir. 
# (Python Enhancement Proposals)
student_name = 'Emre Cevik' # SyntaxError: invalid syntax
```
