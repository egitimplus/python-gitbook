---
description: Indexing & Slicing
---

# Index ve Dilimleme

Listenin elemanlarına index ile ulaşılabilir. Index aynı stringlerde olduğu gibi sıfırdan başlar.

```python
print(my_list[2])    # banana
print(my_list[-1])   # orange 
```

Listelerde dilimleme yapılabilir. Geriye sonuç olarak yine liste döner. Dilimlemeler de stringler ile aynıdır.

```python
print(my_list[1:3]) # ['apple', 'banana']
```

adımlama yapılabilir

```python
print(my_list[::2]) # ['cherry', 'banana']
```

Liste içerisinde bir elemanın olup olmadığını kontrol etmek için "in" kullanılır&#x20;

```python
print('Newyork' in my_list) # False
```
