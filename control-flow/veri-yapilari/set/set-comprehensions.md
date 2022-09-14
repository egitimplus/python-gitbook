# Set comprehensions

```
data = [1, 2, 3, 4, 4, 5, 5]
new_set = set()

for item in data:
    if item % 2 == 0:
        new_set.add(item)

print(new_set)

new_set = {item for item in data if item % 2 == 0}

print(new_set)
```
