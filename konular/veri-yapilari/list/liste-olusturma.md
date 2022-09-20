# Liste oluşturma

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
