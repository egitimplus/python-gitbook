---
description: >-
  Sıralanabilir (ordered), Değiştirilemez (immutable), Tekrarlanabilir
  (duplicate)
---

# Demet

<pre class="language-python"><code class="lang-python">a = tuple()
print(type(a)) # &#x3C;class 'tuple'>

a = ()
print(type(a)) # &#x3C;class 'tuple'>
<strong>
</strong># Elemanı olan demet oluşturma
t = ('a', 'b', 'c', 'd', 'e')
print(type(t)) # &#x3C;type 'tuple'>

# Parantezler içerisindeki tek bir eleman demet değildir.
t2 = ('a')
print(type(t2)) # &#x3C;type 'str'>

# Demet tanımlayabilmek için parantezler içerisinde , olmalıdır
t2 = ('a',)
print(type(t2)) # &#x3C;type 'tuple'>

# Metin'den demet oluşturma
t = tuple('lupins')
print(print(t)) # ('l', 'u', 'p', 'i', 'n', 's')

# Demetler değiştirilemezler
t = (1, 4, 9)
t[0] = 2
# TypeError: 'tuple' object does not support item assignment

# Demetlerin elemanlarına indexi ile ulaşılabilir. 
print(t[1]) # 4
print(t[-1]) # 9</code></pre>
