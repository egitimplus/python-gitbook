# Builtin Fonksiyonlar

## range()

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

## enumerate()

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

## zip()

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
