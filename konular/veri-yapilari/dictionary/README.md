---
description: >-
  Sıralanabilir (ordered), Değiştirilebilir (mutable), Tekrarlanamaz (not
  duplicate)
---

# Sözlük

## Creating Dictionary

Rules for creating a dictionary:

* Every key must be unique (otherwise it will be overridden)
* Every key must be hashable (can use the hash function to hash it; otherwise TypeError will be thrown)
* There is no particular order for the keys.

```python
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

```python
dict(a=1, b=2, c=3) # {'a': 1, 'b': 2, 'c': 3}Py
dict([('d', 4), ('e', 5), ('f', 6)]) # {'d': 4, 'e': 5, 'f': 6}
dict([('a', 1)], b=2, c=3) # {'a': 1, 'b': 2, 'c': 3}
dict({'a' : 1, 'b' : 2}, c=3) # {'a': 1, 'b': 2, 'c': 3}
```

```python
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

```python
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
