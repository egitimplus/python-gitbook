# Değişkenler

{% hint style="warning" %}
değişken oluşturma
{% endhint %}

```python
x = 5
y = "John"

print(x)
print(y)
```

```
Output:
----------------------------------------
5
John
```

{% hint style="warning" %}
değişken tanımlama kuralları
{% endhint %}

<pre class="language-python"><code class="lang-python">'''
Harf veya alt çizgi ( _ ) ile başlamalıdır.
Harf, alt çizgi ( _ ) ve rakamlardan oluşabilir.
Kelimeler arasında boşluk bırakılamaz.
'''

# Büyük / küçük harf duyarlıdır.
Hello = 'Hello'
print(hello)

# Python tarafından ayrılmış kelimeler (reserved words) kullanılamaz.
<strong># import keyword
</strong># print(keyword.kwlist)
class = '12-A'

# Türkçe karakterler kullanılabilir ancak kullanılmaması daha iyi olacaktır
adı = 'Emre'
print(adı)

# İsimlendirme yaparken değişken isimlerini tamamen küçük harfle ve aralarında 
# alt çizgi (snake case) kullanılması tavsiye edilir. 
# (Python Enhancement Proposals)
student_name = 'Emre Cevik'</code></pre>
