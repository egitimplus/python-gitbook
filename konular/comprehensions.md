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

```
numbers = []
for x in range(10):
    if x % 2 == 0:
        temp = x
    else:
        temp = -1
 
    numbers.append(2 * temp + 1)

print(numbers)
# Out: [1, -1, 5, -1, 9, -1, 13, -1, 17, -1]

# The above code is equivalent to:

[2 * (x if x % 2 == 0 else -1) + 1 for x in range(10)]
```

```
# One can combine ternary expressions and if conditions. The ternary operator works on the filtered result:

[x if x > 2 else '*' for x in range(10) if x % 2 == 0]
# Out: ['*', '*', 4, 6, 8]

# The same couldn't have been achieved just by ternary operator only:
[x if (x > 2 and x % 2 == 0) else '*' for x in range(10)]
# Out:['*', '*', '*', '*', 4, '*', 6, '*', 8, '*']
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

## Tuple Comprehensions

```
#  Comprehensions involving tuples

[x + y for x, y in [(1, 2), (3, 4), (5, 6)]]
# Out: [3, 7, 11]

[x + y for x, y in zip([1, 3, 5], [2, 4, 6])]
# Out: [3, 7, 11]

# This is just like regular for loops:

for x, y in [(1,2), (3,4), (5,6)]:
    print(x+y)

# Note however, if the expression that begins the comprehension is a tuple then
# it must be parenthesized:

[x, y for x, y in [(1, 2), (3, 4), (5, 6)]]
# SyntaxError: invalid syntax

[(x, y) for x, y in [(1, 2), (3, 4), (5, 6)]]
# Out: [(1, 2), (3, 4), (5, 6)]
```

## Dict Comprehensions

```python
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
```

## Nested List Comprehensions

```python
# Nested List Comprehensions

#List Comprehension with nested loop
[x + y for x in [1, 2, 3] for y in [3, 4, 5]]
#Out: [4, 5, 6, 5, 6, 7, 6, 7, 8]

#Nested List Comprehension
[[x + y for x in [1, 2, 3]] for y in [3, 4, 5]]
#Out: [[4, 5, 6], [5, 6, 7], [6, 7, 8]]

l = []
for y in [3, 4, 5]:
    temp = []
    for x in [1, 2, 3]:
        temp.append(x + y)
    l.append(temp)

# Out: [[4, 5, 6], [5, 6, 7], [6, 7, 8]]


# Transpose Matrix

matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
    ]
    
[[row[i] for row in matrix] for i in range(len(matrix))]
# [[1, 4, 7], [2, 5, 8], [3, 6, 9]]

# For iterating more than two lists simultaneously within list comprehension, one may use zip() as:

list_1 = [1, 2, 3 , 4]
list_2 = ['a', 'b', 'c', 'd']
list_3 = ['6', '7', '8', '9']
# Two lists
[(i, j) for i, j in zip(list_1, list_2)]
# Out: [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]
# Three lists
[(i, j, k) for i, j, k in zip(list_1, list_2, list_3)]
# Out: [(1, 'a', '6'), (2, 'b', '7'), (3, 'c', '8'), (4, 'd', '9')]

[x.sort() for x in [[2, 1], [4, 3], [0, 1]]]
# [None, None, None]

[sorted(x) for x in [[2, 1], [4, 3], [0, 1]]]
# [[1, 2], [3, 4], [0, 1]]

[x for x in 'foo' if x not in 'bar'] # ['f', 'o', 'o']

# with list comprehension
alist = [[[1,2],[3,4]], [[5,6,7],[8,9,10], [12, 13, 14]]]

[col for row in alist for col in row]
# [[1, 2], [3, 4], [5, 6, 7], [8, 9, 10], [12, 13, 14]]
```
