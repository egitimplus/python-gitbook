# Sort

sorting list ascending

```python
data = ['paris', 'istanbul', 'Newyork', 'berlin']


def sort_list(data):
    new = data.copy()
    new.sort()
    return new


print(sort_list(data))
# Output : ['Newyork', 'berlin', 'istanbul', 'paris']
```

sorting list ascending (fix uppercase char problem)

```python
def sort_list(data):
    new = [item.lower() for item in data]
    new.sort()
    return new

print(sort_list(data))
# Output : ['berlin', 'istanbul', 'Newyork', 'paris']
```

sorting list ascending with key parameter

```python
def sort_list(data):
    new = data.copy()
    new.sort(key=lambda x: x.lower())
    return new


print(sort_list(data))
# Output : ['berlin', 'istanbul', 'Newyork', 'paris']
```

sorting list descending

```python
def sort_list(data):
    new = data.copy()
    new.sort(key=lambda x: x.lower(), reverse=True)

    return new


print(sort_list(data))
# Output : ['paris', 'Newyork', 'istanbul', 'berlin']
```

sorting list with sorted method

```python
def sort_list(data):
    new = sorted(data, key=lambda x: x.lower(), reverse=True)
    return new


print(sort_list(data))
# Output : ['paris', 'Newyork', 'istanbul', 'berlin']
```

sorting list by number of characters

```python
def sort_list(data):
    new = data.copy()
    new.sort(key=len)

    return new


print(sort_list(data))

# Output : ['paris', 'berlin', 'Newyork', 'istanbul']
```

```python
def sort_list(data):
    new = data.copy()
    new.sort(key=lambda x: len(x))
    return new


print(sort_list(data))
# Output : ['paris', 'berlin', 'Newyork', 'istanbul']
```

sorting list by second word

```python
data = ['Adam Smith', 'Alex Mors', 'Mina Moore', 'Arya Stark', 'Ban Ate']


def sort_list(data):
    new = data.copy()
    new.sort(key=lambda x: x.split()[1])
    return new


print(sort_list(data))
# Output : ['Ban Ate', 'Mina Moore', 'Alex Mors', 'Adam Smith', 'Arya Stark']
```

sorting list ascending but zeros at the end.

```python
data = [24, 0, 35, 0, 41, 11, 8]


def sorted_list(data):
    new = []
    for item in sorted(data):
        if item != 0:
            new.append(item)

    zero_count = len(data) - len(new)
    if zero_count > 0:
        for i in range(zero_count):
            new.append(0)
    return new


print(sorted_list(data))
# Output : [8, 11, 24, 35, 41, 0, 0]
```
