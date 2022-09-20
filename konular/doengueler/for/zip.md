# zip()

```python
mylist1 = [1,2,3]
mylist2 = ['a','b','c']

# This one is also a generator! We will explain this later, but for 
# now let's transform it to a list
print(zip(mylist1,mylist2)) # <zip at 0x1d205086f08>

print(list(zip(mylist1,mylist2))) # [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd'), (5, 'e')]

for key, value in zip(mylist1,mylist2):
    print(f"key: {key}, value: {value}")

'''
key: 1, value: a
key: 2, value: b
key: 3, value: c
'''
```
