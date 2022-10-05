---
description: >-
  Sıralanabilir (ordered), Değiştirilebilir (mutable), Tekrarlanabilir
  (duplicate)
---

# Liste

* Sıralanabilir (ordered) : Öğelerin belirli bir sıraya sahip olduğu ve bu sıranın değişmeyeceği anlamına gelir. İndexler ile istenilen öğeye ulaşılabilir.
* Değiştirilebilir (mutable) : Listeler oluşturulduktan sonra elemanları değiştirilebilir, yeni eleman eklenebilir ve elemanlar silinebilir.
* Tekrarlanabilir (duplicate) : Listelerde aynı elemanlardan birden fazla bulunabilir.

## Oluşturma

Liste oluşturmak için list() veya \[] kullanılır.

Boş liste oluşturma

```python
# Boş Liste Tanımlama
my_list = list()
my_list = []
```

Elemanı olan liste oluşturma

```python
my_list = ['Newyork', 'London', 'Paris']
print(my_list)
```

Listelere farklı türlerde eleman eklenebilir

```python
my_list = ['Newyork', 3, 3.5, True, ['banana', 'orange']]
print(my_list) 
```

Listenin eleman sayısı için len() fonksiyonu kullanılır.

```python
print(len(my_list)) # 3
```

Listede bir elemanın olup olmadığını kontrol etmek için «in» kullanılır.

```python
if 'Newyork' in my_list:
    pass
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

```python
my_list[1:4] = ['Group']
print(my_list) # ['Newyork', 'Group']
```

Listeye yeni eleman eklemek için append() metodu kullanılır. Yeni eleman en sona eklenir.

```python
my_list.append('Paris')
print(my_list) # ['Newyork', 'Group', 'Paris']
```

Araya eleman eklemek için insert metodu kullanılır.

```python
my_list.insert(1, 'New')
print(my_list) # ['Newyork', 'New', 'Group', 'Paris']
```

extend() metodu ile iki liste birleştirilebilir.

```python
list1 = ['banana', 'orange']
list2 = ['cherry', 'apple']

list1.extend(list2)
print(list1)    # ['banana', 'orange', 'cherry', 'apple']
```

\+ ile iki liste birleştirilebilir.

```python
new_list = list1 + list2
print(new_list) # ['banana', 'orange', 'cherry', 'apple']
```

## Silme

listeden değeri kullanılarak eleman silmek için remove() metodu kullanılır.

```python
new_list.remove('banana')
print(new_list) # ['orange', 'cherry', 'apple']py
```

En sondaki elemanı silmek için pop() kullanılır.  Argüman olarak indeks değeri girerek istediğimiz elemanı da silebiliriz.

```python
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

```python
my_list.clear()
print(my_list) # []
```

## Mutable & Immutable

Be careful when placing mutable objects, such as lists, inside tuples. This may lead to very confusing outcomes when changing them. Will both raise an error and change the contents of the list within the tuple. For example:

```python
t = (1, 2, 3, [1, 2, 3])
t[3] += [4, 5]

# TypeError: 'tuple' object does not support item assignment

print(t) # (1, 2, 3, [1, 2, 3, 4, 5])
```

## Kopyalama

You can slice it:

```python
new_list = my_list[:]
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

You can use the built in list() function:

```python
new_list = list(my_list)
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

You can use the list copy() method:

```python
new_list = my_list.copy()  # Returns a shallow copy of the list
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

You can use copy module:

```python
import copy
new_list = copy.copy(my_list) #inserts references to the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```python
new_list = copy.deepcopy(old_list) #inserts copies of the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

## Sıralama

sort() metodu ile listeleri sıralayabiliriz.

```python
my_list = ['orange', 'banana', 'apple', 'cherry']

my_list.sort()
print(my_list) # ['apple', 'banana', 'cherry', 'orange']

my_list.sort(reverse=True)
print(my_list) # ['orange', 'cherry', 'banana', 'apple']
```

## Karşılaştırma

Comparison of list

```python
[1, 10, 100] < [2, 10, 100]     # True, because 1 < 2
[1, 10, 100] < [1, 10, 100]     # False, because the lists are equal
[1, 10, 100] <= [1, 10, 100]    # True, because the lists are equal
[1, 10, 100] < [1, 10, 101]     # True, because 100 < 101
[1, 10, 100] < [0, 10, 100]     # False, because 0 < 1
[1, 10] < [1, 10, 100]          # True, If one of the lists is contained at the start of the other, the shortest list wins.
```

## Metodlar

### count

```python
my_list = ['orange', 'banana', 'apple', 'cherry']
print(my_list.count('orange')) # 1
```

### index

<pre class="language-python"><code class="lang-python"><strong>my_list = ['orange', 'banana', 'apple', 'cherry']
</strong><strong>print(my_list.index('orange')) # 0</strong></code></pre>

### reverse

```python
my_list = ['orange', 'banana', 'apple', 'cherry']

print(list(reversed(my_list))) # ['cherry', 'apple', 'banana', 'orange']

print(my_list[::-1]) # ['cherry', 'apple', 'banana', 'orange']

my_list.reverse()
print(my_list) # ['cherry', 'apple', 'banana', 'orange']
```

## Nested Lists

Accessing values in nested list

```python
alist = [[[1,2],[3,4]], [[5,6,7],[8,9,10], [12, 13, 14]]]

# Accesses second element in the first list in the first list
print(alist[0][0][1]) #2

# Accesses the third element in the second list in the second list
print(alist[1][1][2]) #10
```

Using nested for loops to print the list:

```python
for row in alist: #One way to loop through nested lists
    for col in row:
        print(col)
```

```python
# Another way to use nested for loops. The other way is better but I've needed to use this on occasion:
for row in range(len(alist)): # A less Pythonic way to loop through lists
    for col in range(len(alist[row])):
        print(alist[row][col])
```

## Comprehensions

```python
data = [1, 2, 3, 4, 4, 5, 5]
new_list = []
  
for item in data:
    if item % 2 == 0:
        new_list.append(item ** 2)
  
print(new_list) # [4, 16, 16] 

new_list = [item ** 2 for item in data if item % 2 == 0]

print(new_list) # [4, 16, 16]
```

```python
# Get a list of uppercase characters from a string
new_list = [s.upper() for s in "Hello World"]
print(new_list)
# ['H', 'E', 'L', 'L', 'O', ' ', 'W', 'O', 'R', 'L', 'D']

# Strip off any commas from the end of strings in a list
new_list = [w.strip(',') for w in ['these,', 'words,,', 'mostly', 'have,commas,']]
print(new_list)
# ['these', 'words', 'mostly', 'have,commas']

# Organize letters in words more reasonably - in an alphabetical order
sentence = "Beautiful is better than ugly"
new_list = ["".join(sorted(word, key = lambda x: x.lower())) for word in sentence.split()]
print(new_list)
# ['aBefiltuu', 'is', 'beertt', 'ahnt', 'gluy']
```

```python
# create a list of characters in apple, replacing non vowels with '*'

# Ex - 'apple' --> ['a', '*', '*', '*' ,'e']
new_list = [x for x in 'apple' if x in 'aeiou' else '*']
print(new_list)
#SyntaxError: invalid syntax

# When using if/else together use them before the loop
new_list = [x if x in 'aeiou' else '*' for x in 'apple']
print(new_list)
#['a', '*', '*', '*', 'e']
```

```python
# Double Iteration

def foo(i):
    return i, i + 0.5

def f():
    for i in range(3):
        for x in foo(i):
            yield str(x)

new = [str(x)
    for i in range(3)
    for x in foo(i)
]

print(new) # ['0', '0.5', '1', '1.5', '2', '2.5']
```



## Nested List Comprehensions

```python
# Nested List Comprehensions

#List Comprehension with nested loop
[x + y for x in [1, 2, 3] for y in [3, 4, 5]]
#Out: [4, 5, 6, 5, 6, 7, 6, 7, 8]

#Nested List Comprehension
[[x + y for x in [1, 2, 3]] for y in [3, 4, 5]]
#Out: [[4, 5, 6], [5, 6, 7], [6, 7, 8]]

l = []
for y in [3, 4, 5]:
    temp = []
    for x in [1, 2, 3]:
        temp.append(x + y)
    l.append(temp)

# Out: [[4, 5, 6], [5, 6, 7], [6, 7, 8]]


# Transpose Matrix

matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
    ]
    
[[row[i] for row in matrix] for i in range(len(matrix))]
# [[1, 4, 7], [2, 5, 8], [3, 6, 9]]

# For iterating more than two lists simultaneously within list comprehension, one may use zip() as:

list_1 = [1, 2, 3 , 4]
list_2 = ['a', 'b', 'c', 'd']
list_3 = ['6', '7', '8', '9']
# Two lists
[(i, j) for i, j in zip(list_1, list_2)]
# Out: [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]
# Three lists
[(i, j, k) for i, j, k in zip(list_1, list_2, list_3)]
# Out: [(1, 'a', '6'), (2, 'b', '7'), (3, 'c', '8'), (4, 'd', '9')]

[x.sort() for x in [[2, 1], [4, 3], [0, 1]]]
# [None, None, None]

[sorted(x) for x in [[2, 1], [4, 3], [0, 1]]]
# [[1, 2], [3, 4], [0, 1]]

[x for x in 'foo' if x not in 'bar'] # ['f', 'o', 'o']

# with list comprehension
alist = [[[1,2],[3,4]], [[5,6,7],[8,9,10], [12, 13, 14]]]

[col for row in alist for col in row]
# [[1, 2], [3, 4], [5, 6, 7], [8, 9, 10], [12, 13, 14]]
```

## any() & all()

```python
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

## min(), max(), sum()

```python
vals = [1, 4, 12, 5]

print(max(vals)) # 12
print(min(vals)) # 1
print(sum(vals)) # 22

```
