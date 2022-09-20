# Ekleme, Güncelleme, Silme



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

extend() metodu ve + ile iki liste birleştirilebilir.

```
list1 = ['banana', 'orange']
list2 = ['cherry', 'apple']

new_list = list1 + list2
print(new_list) # ['banana', 'orange', 'cherry', 'apple']

list1.extend(list2)
print(list1)    # ['banana', 'orange', 'cherry', 'apple']
```

listeden değeri kullanılarak eleman silmek için remove() metodu kullanılır.

```
new_list.remove('banana')
print(new_list) # ['orange', 'cherry', 'apple']
```

En sondaki elemanı silmek için pop() kullanılır.  Argüman olarak indeks değeri girerek istediğimiz elemanı da silebiliriz.

```
print(new_list.pop())     # apple
print(new_list.pop(0))    # orange

```

del komutu ile de istediğimiz elemanı veya listenin tamamını silebiliriz.

```python
my_list = ['Newyork', 3, 3.5, True, ['banana', 'orange']]

del my_list[0]
print(my_list) # [3, 3.5, True, ['banana', 'orange']]
```

clear() metodu ile listeyi temizleyebiliriz

```
my_list.clear()
print(my_list) # []
```
