# Duplicate

```python
data = ['paris', 'istanbul', 'newyork', 'paris', 'berlin', 'paris', 'newyork']
```

The function should check if the list has any duplicates. If there are duplicates, the function should return the duplicates. If there are no duplicates, the function should return "no duplicates".

```python
def find_duplicates(data):
    new = []
    for item in data:
        if data.count(item) > 1:
            if not new.count(item):
                new.append(item)

    return new

print(find_duplicates(data))
# Output: ['paris', 'newyork']
```

```python
def find_duplicates(data):
    new = set()
    for item in data:
        if data.count(item) > 1:
            new.add(item)

    return list(new)
    
print(find_duplicates(data))
# Output: ['paris', 'newyork']
```
