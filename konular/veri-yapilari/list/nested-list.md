# Nested List

```python
# Accessing values in nested list
alist = [[[1,2],[3,4]], [[5,6,7],[8,9,10], [12, 13, 14]]]

# Accesses second element in the first list in the first list
print(alist[0][0][1]) #2

# Accesses the third element in the second list in the second list
print(alist[1][1][2]) #10
```

```python
# Using nested for loops to print the list:
for row in alist: #One way to loop through nested lists
    for col in row:
        print(col)
'''
[1, 2]
[3, 4]
[5, 6, 7]
[8, 9, 10]
[12, 13, 14]
'''
```

```python
# Another way to use nested for loops. The other way is better but I've needed to use this on occasion:
for row in range(len(alist)): # A less Pythonic way to loop through lists
    for col in range(len(alist[row])):
        print(alist[row][col])

'''
[1, 2]
[3, 4]
[5, 6, 7]
[8, 9, 10]
[12, 13, 14]
'''
```
