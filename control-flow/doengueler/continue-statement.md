# continue statement

kendisinden sonra gelen tüm kodların es geçilip döngüye kaldığı yerden devam edilmesini sağlar.

```python
x = 0
result = 0

while x < 100:
    x += 1
    if x % 2 == 0:
        continue
        
    result += x

print(result)
```

```
2500
```
