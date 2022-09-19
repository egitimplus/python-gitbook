# Örnekler

{% hint style="info" %}
```
# 1’den 20’e kadar olan çift sayıları yazdırınız.
```
{% endhint %}

```python
i = 1
while i < 20:
    if i % 2 == 0:
        print(i) 
    i = i + 1

'''
2
4
6
8
10
12
14
16
18
'''
```

{% hint style="info" %}
```
while döngüsü ile aşağıdaki şekli yapınız

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
    
'''
*
**
***
****
*****
'''
```

{% hint style="info" %}
<pre><code><strong>while döngüsü ile aşağıdaki şekli yapınız
</strong>
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5 </code></pre>
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
    
'''
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5 
'''
```
