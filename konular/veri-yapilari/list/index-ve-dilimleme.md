---
description: Indexing & Slicing
---

# Index ve Dilimleme

```python
# Listenin elemanlarına indexi ile ulaşılabilir. 
# Index aynı stringlerde olduğu gibi sıfırdan başlar.
print(my_list[2])
print(my_list[-1])

# Listelerde dilimleme yapılabilir. Geriye sonuç olarak yine liste döner. 
# Dilimlemeler de stringler ile aynıdır.
print(my_list[1:3])

# adımlama yapılabilir
print(my_list[::2])

# Liste içerisinde bir elemanın olup olmadığını kontrol etmek için "in"
# kullanılır
print('Newyork' in my_list)
```

```
banana
orange
['apple', 'banana']
['cherry', 'banana']
False
```
