# degişkenler

Geçici olarak veri saklamak için oluşturduğumuz alanlara değişken denir. Bir değişkene değer atamak için eşittir ( = ) kullanılır. Python’da değişkenlerin tipini önceden tanımlamak gerekmez.

## değişken oluşturma

```python
x = 5       
y = "John"  

print(x) # 5
print(y) # John
```

## değişken tanımlama kuralları

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

## değişken isimlendirme yöntemleri

<table><thead><tr><th width="167">Yöntem</th><th width="166">Örnek</th><th>Kullanım</th></tr></thead><tbody><tr><td>Camel Case</td><td>totalCount</td><td></td></tr><tr><td>Pascal Case</td><td>TotalCount</td><td>sınıflar</td></tr><tr><td>Snake Case</td><td>total_count</td><td>değişken, fonksiyon</td></tr><tr><td>Flat Case</td><td>totalcount</td><td>paket isimleri</td></tr><tr><td>Constant Case</td><td>TOTAL_COUNT</td><td>sabitler</td></tr><tr><td>Kebap Case</td><td>total-count</td><td></td></tr></tbody></table>

```


```
