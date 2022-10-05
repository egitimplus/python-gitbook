# Reverse



Listeyi tersine çeviren kodu yazınız

```
data = ['paris', 'istanbul', 'Newyork', 'berlin']

def list_reverse(data):
    new = data.copy()
    new.reverse()

    return new

print(list_reverse(data))
```

```
def list_reverse(data):
    return data[::-1]

print(list_reverse(data))
```

Bir fonksiyon yazalım ve bu fonksiyon parametre olarak girilen sayıların ortalamasını alsın

```
def my_avg(*numbers):
    return sum(numbers) / len(numbers)

my_avg(3,5,7,10) 
```
