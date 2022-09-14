# else statement

eğer döngü normal olarak tamamlanırsa else bölümü çalıştırılır.

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
```

```
Enter number:100
number is not prime
can divide 2
```
