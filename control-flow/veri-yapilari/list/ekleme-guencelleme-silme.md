# Ekleme, Güncelleme, Silme

```python
# Listede bir elemanın değerini değiştirmek için bulunduğu indexe 
# yeni değer atanır.
my_list[1] = 'Python'
print(my_list)

my_list[1:4] = ['Group']
print(my_list)

# Listeye yeni eleman eklemek için append() metodu kullanılır. 
# Yeni eleman en sona eklenir.
my_list.append('Paris')
print(my_list)

# Araya eleman eklemek için insert metodu kullanılır.
my_list.insert(1, 'New')
print(my_list)

# extend() metodu ve + ile iki liste birleştirilebilir.
list1 = ['banana', 'orange']
list2 = ['cherry', 'apple']

new_list = list1 + list2
print(new_list)

list1.extend(list2)
print(list1)

# listeden değeri kullanılarak eleman silmek için remove() metodu kullanılır.
new_list.remove('banana')
print(new_list)

# En sondaki elemanı silmek için pop() kullanılır. 
# Argüman olarak indeks değeri girerek istediğimiz elemanı da silebiliriz.
print(new_list.pop())
print(new_list.pop(0))
print(new_list)

# del komutu ile de istediğimiz elemanı veya listenin tamamını silebiliriz.
my_list = ['Newyork', 3, 3.5, True, ['banana', 'orange']]

del my_list[0]
print(my_list)

my_list.clear()
print(my_list)
```

```
['Newyork', 'Python', 'Group', 'Paris']
['Newyork', 'Group']
['Newyork', 'Group', 'Paris']
['Newyork', 'New', 'Group', 'Paris']
['banana', 'orange', 'cherry', 'apple']
['banana', 'orange', 'cherry', 'apple']
['orange', 'cherry', 'apple']
apple
orange
['cherry']
[3, 3.5, True, ['banana', 'orange']]
[]
```

```python
# copy

# You can slice it:
new_list = my_list[:]
print(new_list)

# You can use the built in list() function:
new_list = list(my_list)
print(new_list) 

new_list = my_list.copy()  # Returns a shallow copy of the lis
print(new_list)

# You can use copy module:

import copy
new_list = copy.copy(my_list) #inserts references to the objects found in the original.
print(new_list)

new_list = copy.deepcopy(old_list) #inserts copies of the objects found in the original.
print(new_list)

```

```
['Newyork', 3, 3.5, True, ['banana', 'orange']]
['Newyork', 3, 3.5, True, ['banana', 'orange']]
['Newyork', 3, 3.5, True, ['banana', 'orange']]
['Newyork', 3, 3.5, True, ['banana', 'orange']]
['Newyork', 3, 3.5, True, ['banana', 'orange']]
```
