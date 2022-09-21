---
description: >-
  Sıralanabilir (ordered), Değiştirilebilir (mutable), Tekrarlanamaz (not
  duplicate)
---

# Sözlük

```python
my_dict = {'key1':'value1','key2':'value2'}

# Call values by their key
print(my_dict['key2']) # 'value2'

# Its important to note that dictionaries are very flexible in the data types they can hold. 
my_dict = {
    'key1':123,
    'key2':[12,23,33],
    'key3':['item0','item1','item2']
    }

# Let's call items from the dictionary 
print(my_dict['key3']) # ['item0', 'item1', 'item2']

# Can call an index on that value
print(my_dict['key3'][0]) # 'item0'

# Can then even call methods on that value
print(my_dict['key3'][0].upper()) # 'ITEM0'
```

```python
# We can also create keys by assignment. For instance if we started off with an empty dictionary, we could continually add to it:

# Create a new dictionary
d = {}
# Create a new key through assignment
d['animal'] = 'Dog'
d['answer'] = 42
#Show
print(d) # {'animal': 'Dog', 'answer': 42}
```

```python
# Dictionary nested inside a dictionary nested inside a dictionary
d = {'key1':{'nestkey':{'subnestkey':'value'}}}

# Keep calling the keys
print(d['key1']['nestkey']['subnestkey']) # value
```
