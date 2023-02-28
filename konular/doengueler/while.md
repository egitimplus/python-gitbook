# while

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
