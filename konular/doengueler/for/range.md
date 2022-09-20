# range()

İstenilen aralıkta ardışık sayılardan oluşan bir liste oluşturmaya yarar.

range(başlangıç, bitiş, basamak)

{% hint style="info" %}
0’dan başlayıp 5’e kadar sayıları yazdırınız.
{% endhint %}

```python
for number in range(5):
    print(number)
    
'''
0
1
2
3
4
'''
```

{% hint style="info" %}
6’dan başlayıp 21’e kadar 3’er artan dizi oluşturalım
{% endhint %}

```python
for number in range(6, 21, 3):
    print(number)
    
'''
6
9
12
15
18
'''
```
