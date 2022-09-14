# Dict comprehensions

```
data = [1, 2, 3, 4, 4, 5, 5]
new_dict = {}
  
for item in data:
    if item % 2 != 0:
        new_dict[item] = item ** 2

print(new_dict)

new_dict = {item:item ** 2 for item in data if item % 2 != 0}

print(new_dict)
```

```
{1: 1, 3: 9, 5: 25}
{1: 1, 3: 9, 5: 25}
```

```
data = {
    'germany': 'berlin',
    'greece': 'atina',
    'turkey': 'ankara'
}

new_dict = {}
for k,v in data.items():
    new_dict[k[:3]] = v

print(new_dict)

new_dict = {k[:3]:v for k,v in data.items()}

print(new_dict)
```

```
{'ger': 'berlin', 'gre': 'atina', 'tur': 'ankara'}
{'ger': 'berlin', 'gre': 'atina', 'tur': 'ankara'}
```

```
# Merging Dictionaries

dict1 = {'w': 1, 'x': 1}
dict2 = {'x': 2, 'y': 2, 'z': 2}

{k: v for d in [dict1, dict2] for k, v in d.items()} # Out: {'w': 1, 'x': 2, 'y': 2, 'z': 2}

# Python 3.x Version ≥ 3.5

{**dict1, **dict2} # Out: {'w': 1, 'x': 2, 'y': 2, 'z': 2}
```

```
# Nested Loops

data = [[1, 2], [3, 4], [5, 6]]
output = []
for each_list in data:
    for element in each_list:
        output.append(element)
print(output)
# Out: [1, 2, 3, 4, 5, 6]

[element for each_list in data for element in each_list] # Out: [1, 2, 3, 4, 5, 6]

```

```
import timeit

data = [[1,2],[3,4],[5,6]]

# 1000000 loops, best of 3: 1.37 µs per loop
def f():
    output=[]
    for each_list in data:
        for element in each_list:
            output.append(element)
    return output


# 1000000 loops, best of 3: 632 ns per loop
[inner for outer in data for inner in outer]

```
