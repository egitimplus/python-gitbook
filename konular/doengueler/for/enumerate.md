# enumerate()

```
index_count = 0

for letter in 'python':
    print(f"index: {index_count}, letter:{letter }")
    index_count += 1

'''
index: 0, letter:p
index: 1, letter:y
index: 2, letter:t
index: 3, letter:h
index: 4, letter:o
index: 5, letter:n
'''
```

```
for i,letter in enumerate('python'):
    print(f"index: {i}, letter:{letter }")

'''
index: 0, letter:p
index: 1, letter:y
index: 2, letter:t
index: 3, letter:h
index: 4, letter:o
index: 5, letter:n
'''
```
