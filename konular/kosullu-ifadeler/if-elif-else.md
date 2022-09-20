# If - elif - else

## if

{% hint style="info" %}
```
if <condition>:
    ...
    ...
```
{% endhint %}

```python
if True:
    print('condition is true')
    
# Output: condition is true
```

<pre class="language-python"><code class="lang-python"><strong>x = 4
</strong><strong>if x > 5:
</strong>    print('x is greater than 5')</code></pre>

{% hint style="info" %}
Klavyeden girilen sayı pozitif ise ekrana pozitif yazdırınız
{% endhint %}

## else

{% hint style="info" %}
```
if <condition>:
    ...
    ...
else:
    ...
    ...
```
{% endhint %}

```
x = 3
if x > 5:
    print('x is greater than 5')
else:
    print('x is less than 5')

# Output: x is less than 5
```

{% hint style="info" %}
Klavyeden girilen vize ve final sınav notlarından öğrencinin sınıfı geçip geçmediğini tespit eden programı yazınız.&#x20;

Geçme notu : 50&#x20;

Vize katsayısı : %30&#x20;

Final katsayısı: %70
{% endhint %}

## elif

{% hint style="info" %}
```
if <condition>:
    ...
    ...
elif <condition>:
    ...
    ...
else:
    ...
    ...
```
{% endhint %}

```python
x = 4
if x > 5:
    print('x is greater than 5')
elif x > 3:
    print('x is greater than 3')
else:
    print('x is less than 5')
    
# Output: x is greater than 3
```

{% hint style="info" %}
Kullanıcı tarafından girilen sınav puanını nota çeviren programı yazınız. Eğer girilen puan 0-100 aralığında değilse ekrana hata mesajı basınız.


{% endhint %}

| Sınav Puanı | Not |
| ----------- | --- |
| 0-20        | E   |
| 21-40       | D   |
| 41-60       | C   |
| 61-80       | B   |
| 81-100      | A   |

## tek satırda if-else

```python
n = 5
result = "Hello" if n > 10 else "Goodbye" if n > 5 else "Good day"
print(result) 
# Output: Goodbye
```
