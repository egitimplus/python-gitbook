# break - continue - else

## break

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

## continue

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

## else

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
