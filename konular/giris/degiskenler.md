---
description: Variables
---

# Değişkenler

Geçici olarak veri saklamak için oluşturduğumuz alanlara değişken denir. Bir değişkene değer atamak için eşittir ( = ) kullanılır. Python’da değişkenlerin tipini önceden tanımlamak gerekmez.

Örnek : Hızı 115km olan bir araç 5 saatte kaç km yol gider?

Mesafe = Hız x Zaman

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

{% hint style="info" %}
Değişken İsimlendirme Yöntemleri
{% endhint %}

| Yöntem        | Örnek         | Kullanım            |
| ------------- | ------------- | ------------------- |
| Camel Case    | toplamKayit   |                     |
| Pascal Case   | ToplamKayit   | sınıflar            |
| Snake Case    | toplam\_kayit | değişken, fonksiyon |
| Flat Case     | toplamkayit   | paket isimleri      |
| Constant Case | TOPLAM\_KAYIT | sabitler            |
| Kebap Case    | toplam-kayit  |                     |

```



```
