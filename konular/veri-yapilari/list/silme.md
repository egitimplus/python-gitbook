# Silme

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
