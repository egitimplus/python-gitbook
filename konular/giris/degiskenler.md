---
description: Variables
---

# Değişkenler

Geçici olarak veri saklamak için oluşturduğumuz alanlara değişken denir. Bir değişkene değer atamak için eşittir ( = ) kullanılır. Python’da değişkenlerin tipini önceden tanımlamak gerekmez.

Örnek : Hızı 115km olan bir araç 5 saatte kaç km yol gider?

Mesafe = Hız x Zaman

## Değişken oluşturma

```python
x = 5       
y = "John"  

print(x) # 5
print(y) # John
```

## Değişken Tanımlama Kuralları

{% hint style="info" %}
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

## Değişken İsimlendirme Yöntemleri

| Yöntem        | Örnek        | Kullanım            |
| ------------- | ------------ | ------------------- |
| Camel Case    | totalCount   |                     |
| Pascal Case   | TotalCount   | sınıflar            |
| Snake Case    | total\_count | değişken, fonksiyon |
| Flat Case     | totalcount   | paket isimleri      |
| Constant Case | TOTAL\_COUNT | sabitler            |
| Kebap Case    | total-count  |                     |

```


```
