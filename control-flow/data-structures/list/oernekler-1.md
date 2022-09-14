# Örnekler

```python
# Checking if list is empty

lst = []
if not lst:
    print("list is empty")

# Checking whether an item is in a list
lst = ['test', 'twest', 'tweast', 'treast']

print('test' in lst)
# Out: True

print('toast' in lst)
# Out: False
```

```
list is empty
True
False
```

```python
#  Iterating over a list

my_list = ['foo', 'bar', 'baz']
for item in my_list:
    print(item)

# You can also get the position of each item at the same time:
for (index, item) in enumerate(my_list):
    print('The item in position {} is: {}'.format(index, item))

# The other way of iterating a list based on the index value:
for i in range(0,len(my_list)):
    print(i, my_list[i])

# Note that changing items in a list while iterating on it may have unexpected results:

for item in my_list:
    if item == 'foo':
        del my_list[0]
        print(item)
```

```
foo
bar
baz
The item in position 0 is: foo
The item in position 1 is: bar
The item in position 2 is: baz
0 foo
1 bar
2 baz
foo
```

```python
# For mutable elements, the same construct will result in all elements of the 
# list referring to the same object, for example, for a set:

my_list=[{1}] * 10
print(my_list)

my_list[0].add(2)
print(my_list)
```

```
[{1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}, {1}]
[{1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}, {1, 2}]
```

```python
#  Changing Types in a List

# Convert a list of strings to integers.
items = ["1","2","3","4"]
new_list = [int(item) for item in items]
print(new_list)
# Out: [1, 2, 3, 4]

# Convert a list of strings to float.
items = ["1","2","3","4"]
new_list = map(float, items)
print(list(new_list))
# Out:[1.0, 2.0, 3.0, 4.0]

```

```
[1, 2, 3, 4]
[1.0, 2.0, 3.0, 4.0]
```
