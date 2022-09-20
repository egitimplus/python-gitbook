# Ekleme ve Güncelleme



Listede bir elemanın değerini değiştirmek için bulunduğu indexe yeni değer atanır.

```python
my_list = ['Newyork', 'France', 'Group', 'Paris'] 
my_list[1] = 'Python' 
print(my_list) # ['Newyork', 'France', 'Group', 'Paris']
```

Birden fazla değerde değiştirilebilir.

```
my_list[1:4] = ['Group']
print(my_list) # ['Newyork', 'Group']
```

Listeye yeni eleman eklemek için append() metodu kullanılır. Yeni eleman en sona eklenir.

```
my_list.append('Paris')
print(my_list) # ['Newyork', 'Group', 'Paris']
```

Araya eleman eklemek için insert metodu kullanılır.

```
my_list.insert(1, 'New')
print(my_list) # ['Newyork', 'New', 'Group', 'Paris']
```

extend() metodu ile iki liste birleştirilebilir.

```
list1 = ['banana', 'orange']
list2 = ['cherry', 'apple']

list1.extend(list2)
print(list1)    # ['banana', 'orange', 'cherry', 'apple']
```

\+ ile iki liste birleştirilebilir.

```
new_list = list1 + list2
print(new_list) # ['banana', 'orange', 'cherry', 'apple']
```
