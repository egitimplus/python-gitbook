# List

* Sıralanabilir (ordered) : Öğelerin belirli bir sıraya sahip olduğu ve bu sıranın değişmeyeceği anlamına gelir. İndexler ile istenilen öğeye ulaşılabilir.
* Değiştirilebilir (mutable) : Listeler oluşturulduktan sonra elemanları değiştirilebilir, yeni eleman eklenebilir ve elemanlar silinebilir.
* Tekrarlanabilir (duplicate) : Listelerde aynı elemanlardan birden fazla bulunabilir.

## Liste Oluşturma



Liste oluşturmak için list() veya \[] kullanılır.

Boş liste oluşturma

```python
# Boş Liste Tanımlama
my_list = list()
my_list = []
print(my_list) 
# Output: []
```

Elemanı olan liste oluşturma

```
my_list = ['Newyork', 'London', 'Paris']
my_list = list(('Newyork', 'London', 'Paris'))

print(my_list) 
# Output: ['Newyork', 'London', 'Paris']
```

Listelere farklı türlerde eleman eklenebilir

```
my_list = ['Newyork', 3, 3.5, True, ['banana', 'orange']]
print(my_list) 
# Output: ['Newyork', 3, 3.5, True, ['banana', 'orange']]Listenin eleman sayısı için len() fonksiyonu kullanılır.
```

```
print(len(my_list)) 
# Output: 3
```

## Index ve Dilimleme

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

## Ekleme ve Güncelleme



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

## Silme

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

## Kopyalama

```
# You can slice it:
new_list = my_list[:]
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
# You can use the built in list() function:
new_list = list(my_list)
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
new_list = my_list.copy()  # Returns a shallow copy of the lis
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
# You can use copy module:

import copy
new_list = copy.copy(my_list) #inserts references to the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
new_list = copy.deepcopy(old_list) #inserts copies of the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

## Sıralama

```python
# sort() metodu ile listeleri sıralayabiliriz.

my_list = ['orange', 'banana', 'apple', 'cherry']
my_list.sort()
print(my_list)

my_list.sort(reverse=True)
print(my_list)
```

```
['apple', 'banana', 'cherry', 'orange']
['orange', 'cherry', 'banana', 'apple']
```

## Metodlar

```
// Some code
```

## Nested Lists

```
// Some code
```

## List Comprehensions

```
// Some code
```

## any() & all()

```
// Some code
```
