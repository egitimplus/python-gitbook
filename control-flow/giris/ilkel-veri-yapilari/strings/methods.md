# Methods

```python
text = 'hello World AGAIN'

print(text.lower())
print(text.upper())
print(text.capitalize())
print(text.title())
print(text.swapcase())
print('')

print(text.count('e'))
print(text.index('e'))
print(text.find('e'))
print(text.replace('l', 'a', 2))

# strip 
text = '   ?+Hello World +-?'
print(text.strip())
print(text.strip(' -+?'))
print(text.strip(' ?+'))
print(text.lstrip())
print(text.rstrip())
print('')

# split
text = 'Hello World Again and Again'
print(text.split(' '))
print(text.split('World'))
print(text.split(' ', 2))
print(text.rsplit(' ', 2))
print(text.partition('World'))

# conditions
# islower(), isupper(), istitle()
# isalnum(), isalpha(), isspace()
# isdigit(), isnumeric(), isdecimal()
# endswith(), startswith()
```

```
1
1
1
heaao World AGAIN
hello world again
HELLO WORLD AGAIN
Hello world again
Hello World Again
HELLO wORLD again

?+Hello World +-?
Hello World
Hello World +-
?+Hello World +-?
   ?+Hello World +-?

['Hello', 'World', 'Again', 'and', 'Again']
['Hello ', ' Again and Again']
['Hello', 'World', 'Again and Again']
['Hello World Again', 'and', 'Again']
('Hello ', 'World', ' Again and Again')
```
