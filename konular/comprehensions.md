# Comprehensions

## List Comprehensions

```python
data = [1, 2, 3, 4, 4, 5, 5]
new_list = []
  
for item in data:
    if item % 2 == 0:
        new_list.append(item ** 2)
  
print(new_list) # [4, 16, 16] 

new_list = [item ** 2 for item in data if item % 2 == 0]

print(new_list) # [4, 16, 16]
```

```python
# Get a list of uppercase characters from a string
new_list = [s.upper() for s in "Hello World"]
print(new_list)
# ['H', 'E', 'L', 'L', 'O', ' ', 'W', 'O', 'R', 'L', 'D']

# Strip off any commas from the end of strings in a list
new_list = [w.strip(',') for w in ['these,', 'words,,', 'mostly', 'have,commas,']]
print(new_list)
# ['these', 'words', 'mostly', 'have,commas']

# Organize letters in words more reasonably - in an alphabetical order
sentence = "Beautiful is better than ugly"
new_list = ["".join(sorted(word, key = lambda x: x.lower())) for word in sentence.split()]
print(new_list)
# ['aBefiltuu', 'is', 'beertt', 'ahnt', 'gluy']
```

```python
# create a list of characters in apple, replacing non vowels with '*'

# Ex - 'apple' --> ['a', '*', '*', '*' ,'e']
new_list = [x for x in 'apple' if x in 'aeiou' else '*']
print(new_list)
#SyntaxError: invalid syntax

# When using if/else together use them before the loop
new_list = [x if x in 'aeiou' else '*' for x in 'apple']
print(new_list)
#['a', '*', '*', '*', 'e']
```

```python
# Double Iteration

def foo(i):
    return i, i + 0.5

def f():
    for i in range(3):
        for x in foo(i):
            yield str(x)

new = [str(x)
    for i in range(3)
    for x in foo(i)
]

print(new) # ['0', '0.5', '1', '1.5', '2', '2.5']
```
