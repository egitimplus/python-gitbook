# Methods

```python
text = 'hello World AGAIN'

print(text.lower()) # hello world again
print(text.upper()) # HELLO WORLD AGAIN
print(text.capitalize()) # Hello world again
print(text.title()) # Hello World Again
print(text.swapcase()) # HELLO wORLD again
print('')

print(text.count('e')) # 1
print(text.index('e')) # 1
print(text.find('e')) # 1
print(text.replace('l', 'a', 2)) # heaao World AGAIN

# strip 
text = '   ?+Hello World +-?'
print(text.strip()) # ?+Hello World +-?
print(text.strip(' -+?')) # Hello World
print(text.strip(' ?+')) # Hello World +-
print(text.lstrip()) # ?+Hello World +-?
print(text.rstrip()) #    ?+Hello World +-?
print('')

# split
text = 'Hello World Again and Again'
print(text.split(' ')) # ['Hello', 'World', 'Again', 'and', 'Again']
print(text.split('World')) # ['Hello ', ' Again and Again']
print(text.split(' ', 2)) # ['Hello', 'World', 'Again and Again']
print(text.rsplit(' ', 2)) # ['Hello World Again', 'and', 'Again']
print(text.partition('World')) # ('Hello ', 'World', ' Again and Again')

# conditions
# islower(), isupper(), istitle()
# isalnum(), isalpha(), isspace()
# isdigit(), isnumeric(), isdecimal()
# endswith(), startswith()
```
