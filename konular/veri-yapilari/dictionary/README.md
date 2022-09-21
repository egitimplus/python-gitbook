---
description: >-
  Sıralanabilir (ordered), Değiştirilebilir (mutable), Tekrarlanamaz (not
  duplicate)
---

# Sözlük



```python
'''
Creating Dictionary
Rules for creating a dictionary:
- Every key must be unique (otherwise it will be overridden)
- Every key must be hashable (can use the hash function to hash it; otherwise TypeError will be thrown)
- There is no particular order for the keys.
'''

# Creating and populating it with values
stock = {'eggs': 5, 'milk': 2}

# Or creating an empty dictionary
dictionary = {}
# And populating it after
dictionary['eggs'] = 5
dictionary['milk'] = 2

# Values can also be lists
mydict = {'a': [1, 2, 3], 'b': ['one', 'two', 'three']}

# Use list.append() method to add new elements to the values list
mydict['a'].append(4) # => {'a': [1, 2, 3, 4], 'b': ['one', 'two', 'three']}
mydict['b'].append('four') # => {'a': [1, 2, 3, 4], 'b': ['one', 'two', 'three', 'four']}

# We can also create a dictionary using a list of two-items tuples
iterable = [('eggs', 5), ('milk', 2)]
dictionary = dict(iterables)

# Or using keyword argument:
dictionary = dict(eggs=5, milk=2)

# Another way will be to use the dict.fromkeys:
dictionary = dict.fromkeys((milk, eggs)) # => {'milk': None, 'eggs': None}
dictionary = dict.fromkeys((milk, eggs), (2, 5)) # => {'milk': 2, 'eggs': 5}
```

```
dict(a=1, b=2, c=3) # {'a': 1, 'b': 2, 'c': 3}
dict([('d', 4), ('e', 5), ('f', 6)]) # {'d': 4, 'e': 5, 'f': 6}
dict([('a', 1)], b=2, c=3) # {'a': 1, 'b': 2, 'c': 3}
dict({'a' : 1, 'b' : 2}, c=3) # {'a': 1, 'b': 2, 'c': 3}
```

```
# Unpacking dictionaries using the ** operator

def parrot(voltage, state, action):
    print("This parrot wouldn't", action, end=' ')
    print("if you put", voltage, "volts through it.", end=' ')
    print("E's", state, "!")

d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
parrot(**d)

fish = {'name': "Nemo", 'hands': "fins", 'special': "gills"}
dog = {'name': "Clifford", 'hands': "paws", 'color': "red"}
fishdog = {**fish, **dog}
print(fishdog)

```

```
car = {}
car["wheels"] = 4
car["color"] = "Red"
car["model"] = "Corvette"

print(car)

# Dictionary values can be iterated over:
for key in car:
    print(str(key) + ": " + str(car[key]))

# All combinations of dictionary values

options = {
 "x": ["a", "b"],
 "y": [10, 20, 30]
}

import itertools

keys = options.keys()
values = (options[key] for key in keys)
combinations = [dict(zip(keys, combination)) for combination in itertools.product(*values)]
print(combinations)
```

```
data = [1, 2, 3, 4, 4, 5, 5]
new_dict = {}
  
for item in data:
    if item % 2 != 0:
        new_dict[item] = item ** 2

print(new_dict) # {1: 1, 3: 9, 5: 25}

new_dict = {item:item ** 2 for item in data if item % 2 != 0}

print(new_dict) # {1: 1, 3: 9, 5: 25}



data = {
    'germany': 'berlin',
    'greece': 'atina',
    'turkey': 'ankara'
}

new_dict = {}
for k,v in data.items():
    new_dict[k[:3]] = v

print(new_dict) # {'ger': 'berlin', 'gre': 'atina', 'tur': 'ankara'}


new_dict = {k[:3]:v for k,v in data.items()}

print(new_dict) # {'ger': 'berlin', 'gre': 'atina', 'tur': 'ankara'}

# Merging Dictionaries
dict1 = {'w': 1, 'x': 1}
dict2 = {'x': 2, 'y': 2, 'z': 2}

{k: v for d in [dict1, dict2] for k, v in d.items()} # Out: {'w': 1, 'x': 2, 'y': 2, 'z': 2}

# Python 3.x Version ≥ 3.5

{**dict1, **dict2} # Out: {'w': 1, 'x': 2, 'y': 2, 'z': 2}

# Nested Loops

data = [[1, 2], [3, 4], [5, 6]]
output = []
for each_list in data:
    for element in each_list:
        output.append(element)
print(output)
# Out: [1, 2, 3, 4, 5, 6]

[element for each_list in data for element in each_list] # Out: [1, 2, 3, 4, 5, 6]

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
