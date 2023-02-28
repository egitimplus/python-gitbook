---
description: Loops
---

# Döngüler



## While

{% hint style="success" %}
```
while <condition>:
    ...
    ...
    ...
```
{% endhint %}

{% hint style="info" %}
Örnek : 0’dan başlayıp 5’e kadar sayıları yazdırınız.
{% endhint %}

```python
number = 0
while number < 5:
    print('loop working', number)
    number += 1

print('Loop End')

'''
loop working 0
loop working 1
loop working 2
loop working 3
loop working 4
Loop End
'''
```

{% hint style="info" %}
1’den 20’e kadar olan çift sayıları yazdırınız.
{% endhint %}

```python
i = 1
while i < 20:
    if i % 2 == 0:
        print(i) 
    i = i + 1
```

{% hint style="info" %}
while döngüsü ile aşağıdaki şekli yapınız

```
*
**
***
****
*****
```
{% endhint %}

```python
i = 1
while i < 6:
    print(i * '*')
    i = i + 1
```

{% hint style="info" %}
while döngüsü ile aşağıdaki şekli yapınız

```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5 
```
{% endhint %}

```python
i = 1
while i < 6:
    j = 1
    while j < i + 1: 
        print(j, end=' ')
        j = j + 1
        
    i = i + 1
    print('')
```

## For



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

## Builtin Fonksiyonlar



### range()

İstenilen aralıkta ardışık sayılardan oluşan bir liste oluşturmaya yarar.

{% hint style="info" %}
0’dan başlayıp 5’e kadar sayıları yazdırınız.
{% endhint %}

```
for number in range(5):
    print(number)
```

{% hint style="info" %}
6’dan başlayıp 21’e kadar 3’er artan dizi oluşturalım
{% endhint %}

```
for number in range(6, 21, 3):
    print(number)
```

### enumerate()

```
index_count = 0

for letter in 'python':
    print(f"index: {index_count}, letter:{letter}")
    index_count += 1

'''
index: 0, letter:p
...
index: 5, letter:n
'''
```

```
for i,letter in enumerate('python'):
    print(f"index: {i}, letter:{letter }")
```

### zip()

```
mylist1 = [1,2,3]
mylist2 = ['a','b','c']

# This one is also a generator! We will explain this later, but for 
# now let's transform it to a list
print(zip(mylist1,mylist2)) # <zip at 0x1d205086f08>

print(list(zip(mylist1,mylist2))) # [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd'), (5, 'e')]

for key, value in zip(mylist1,mylist2):
    print(f"key: {key}, value: {value}")

'''
key: 1, value: a
key: 2, value: b
key: 3, value: c
'''
```

## Atlama İfadeleri



### break

devam eden bir süreci kesintiye uğratmak için kullanılır.

```python
while True:
    username = input('Enter username : ')
    if len(username) < 4:
        print('Username cannot be less than 4 characters')
    else:
        print('Successfully')
        break
        
'''
Enter username : asdsad
Successfully
'''
```

### continue

kendisinden sonra gelen tüm kodların es geçilip döngüye kaldığı yerden devam edilmesini sağlar.

```python
x = 0
result = 0

while x < 100:
    x += 1
    if x % 2 == 0:
        continue
        
    result += x

print(result) # 2500
```

### else

eğer döngü normal olarak tamamlanırsa else bölümü çalıştırılır.

{% hint style="info" %}
Kullanıcı tarafından girilen sayının asal olup olmadığını tespit eden programı yazınız.
{% endhint %}

```python
i = 2
number = int(input('Enter number:'))
while i < number:
    if number % i == 0:
        print('number is not prime')
        print('divisible by', i)
        break
    i += 1
else:
    print('number is prime')
    
'''
Enter number:100
number is not prime
can divide 2
'''
```
