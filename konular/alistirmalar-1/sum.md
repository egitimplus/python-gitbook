# Sum

{% hint style="info" %}
Sum of numbers in the list
{% endhint %}

```python
def sum_numbers(data):
    sum = 0
    for number in data:
        sum += int(number)

    return sum

print(sum_numbers(numbers)) 
# Output : 41
```

```python
def sum_numbers(data):
    new = []
    for number in data:
        new.append(int(number))

    return sum(new)

print(sum_numbers(numbers)) 
# Output : 41
```

```python
def sum_numbers(data):
    result = sum([int(item) for item in data])
    return result
  
print(sum_numbers(numbers)) 
# Output : 41
```

```python
def sum_numbers(data):
    result = sum(map(lambda x: int(x), data))
    return result
  
print(sum_numbers(numbers))
# Output : 41
```

```python
from functools import reduce

def sum_numbers(data):
    result = reduce(lambda x, y: int(x) + int(y), data)
    return result
  
print(sum_numbers(numbers))
# Output : 41
```

{% hint style="info" %}
if non-number characters
{% endhint %}

```python
numbers = ['1', 2, '5', '7', '11', 15, 'bla']

def sum_numbers(data):
    new = []
    for number in data:
        if str(number).isdecimal():
            new.append(int(number))

    return sum(new)

print(sum_numbers(numbers)) 
# Output : 41
```

{% hint style="info" %}
Bir fonksiyona gönderilen sayıların toplamını ve benzersiz olanlarının toplamına bölen ve döndüren fonksiyon.
{% endhint %}

```python
def sum_uniques(*numbers):
    unique_sum = 0
    for number in numbers:
        if numbers.count(number) == 1:
            unique_sum += number

    return unique_sum / sum(numbers)
        
sum_uniques(50, 20, 30, 50)
```
