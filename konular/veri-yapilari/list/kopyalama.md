# Kopyalama

```
# You can slice it:
new_list = my_list[:]
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
# You can use the built in list() function:
new_list = list(my_list)
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
new_list = my_list.copy()  # Returns a shallow copy of the lis
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
# You can use copy module:

import copy
new_list = copy.copy(my_list) #inserts references to the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```

```
new_list = copy.deepcopy(old_list) #inserts copies of the objects found in the original.
print(new_list) # ['Newyork', 3, 3.5, True, ['banana', 'orange']]
```
