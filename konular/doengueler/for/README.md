# For

{% hint style="success" %}
```
for variable in iterable:
    ...
    ...
    ...
```
{% endhint %}

{% hint style="info" %}
python kelimesinin harflerini yazdırınız
{% endhint %}

```python
for letter in 'Python':
    print(letter)
```

{% hint style="info" %}
Bir liste içerisindeki elemanları ekrana yazdırınız
{% endhint %}

```python
# We'll learn how to automate this sort of list in the next lecture

list1 = [1,2,3,4,5,6,7,8,9,10]
for num in list1:
    print(num)
```

{% hint style="info" %}
Kullanıcı tarafından girilen sayının faktöryelini hesaplayınız.
{% endhint %}

```python
faktoryel = 3
i = 1
toplam = 1
while i < faktoryel:
    i = i + 1
    toplam = toplam * i
    
print(toplam) # 6
```

{% hint style="info" %}
Klavyeden girilen başlangıç ve bitiş sayıları arasında bulunan tek sayıların ortalamasını bulan programı yazınız.
{% endhint %}

```python
baslangic = 3
bitis = 9

toplam = 0
adet = 0
for i in range(baslangic, bitis):
    if i % 2 != 0:
        toplam = toplam + i
        adet = adet + 1
        
print(toplam / adet) # 5.0
```

{% hint style="info" %}
Klavyeden girilen sayının rakamlarının çarpımını bulan programı yazınız.
{% endhint %}

```python
x = '123123'

toplam = 1
for i in x:
    toplam = int(i) * toplam

print(toplam) # 36
```
