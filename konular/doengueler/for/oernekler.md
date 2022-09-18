# Örnekler

{% hint style="info" %}
```
Kullanıcı tarafından girilen sayının faktöryelini hesaplayınız.
```
{% endhint %}

```python
faktoryel = 3
i = 1
toplam = 1
while i < faktoryel:
    i = i + 1
    toplam = toplam * i
    
print(toplam)
```

```
Output:
----------------------------------------
6
```

{% hint style="info" %}
```
Klavyeden girilen başlangıç ve bitiş sayıları arasında bulunan tek sayıların 
ortalamasını bulan programı yazınız.
```
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
        
print(toplam / adet)
```

```
Output:
----------------------------------------
5.0
```

{% hint style="info" %}
```
Klavyeden girilen sayının rakamlarının çarpımını bulan programı yazınız.
```
{% endhint %}

```python
x = '123123'

toplam = 1
for i in x:
    toplam = int(i) * toplam
    print(toplam)
```

```
Output:
----------------------------------------
1
2
6
6
12
36
```
