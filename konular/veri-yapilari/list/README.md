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

## Karşılaştırma

```
# Comparison of list

[1, 10, 100] < [2, 10, 100]     # True, because 1 < 2
[1, 10, 100] < [1, 10, 100]     # False, because the lists are equal
[1, 10, 100] <= [1, 10, 100]    # True, because the lists are equal
[1, 10, 100] < [1, 10, 101]     # True, because 100 < 101
[1, 10, 100] < [0, 10, 100]     # False, because 0 < 1
[1, 10] < [1, 10, 100]          # True, If one of the lists is contained at the start of the other, the shortest list wins.

```

## Metodlar

```
my_list = ['orange', 'banana', 'apple', 'cherry']

# count
print(my_list.count('orange')) # 1

# index
print(my_list.index('orange')) # 0

# reverse

print(list(reversed(my_list))) # ['cherry', 'apple', 'banana', 'orange']

print(my_list[::-1]) # ['cherry', 'apple', 'banana', 'orange']

my_list.reverse()
print(my_list) # ['cherry', 'apple', 'banana', 'orange']
```

## Nested Lists

```
# Accessing values in nested list
alist = [[[1,2],[3,4]], [[5,6,7],[8,9,10], [12, 13, 14]]]

# Accesses second element in the first list in the first list
print(alist[0][0][1]) #2

# Accesses the third element in the second list in the second list
print(alist[1][1][2]) #10
```

```
# Using nested for loops to print the list:
for row in alist: #One way to loop through nested lists
    for col in row:
        print(col)
```

```
# Another way to use nested for loops. The other way is better but I've needed to use this on occasion:
for row in range(len(alist)): # A less Pythonic way to loop through lists
    for col in range(len(alist[row])):
        print(alist[row][col])
```

## List Comprehensions

```
// Some code
```

## any() & all()

```
# any and all

# You can use all() to determine if all the values in an iterable evaluate to True

nums = [1, 1, 0, 1]
print(all(nums)) # False

chars = ['a', 'b', 'c', 'd']
print(all(chars)) # True

# Likewise, any() determines if one or more values in an iterable evaluate to True

nums = [1, 1, 0, 1]
print(any(nums)) # True

vals = [None, None, None, False]
print(any(vals)) # False

vals = [1, 2, 3, 4]

print(any(val > 12 for val in vals)) # False

print(any((val * 2) > 6 for val in vals)) # True

```
