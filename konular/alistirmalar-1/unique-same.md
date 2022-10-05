# Unique - Same

Get unique values from a list

```
data = ['apple', 'apricot', 'blueberry', 'apple', 'Apple', 
        'apricot', 'blueberry', 'cherry', 'Banana', 'applE']
        
def unique_list(data):
    new = []
    for item in data:
        if not new.count(item.lower()):
            new.append(item.lower())

    return new

print(unique_list(data))
# Output : ['apple', 'apricot', 'blueberry', 'cherry', 'banana']
```

```
def unique_list(data):
    return list(set(i.lower() for i in data))
    
print(unique_list(data))
# Output : ['apricot', 'blueberry', 'banana', 'apple', 'cherry']
```

İki listedeki aynı olan elemanları yazdıran fonksiyon

```
data1 = [1, 2, 5, 10]
data2 = [2, 4, 10, 20]

def same_items(data1, data2):
    new = []
    for item in data1:
        if item in data2:
            new.append(item)

    return new

same_items(data1, data2)
```
