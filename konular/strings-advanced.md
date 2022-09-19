# Strings Advanced

{% tabs %}
{% tab title="Basics" %}
```python
# Output : HelloWorld

print('4' + '2') 
# Output : 42

print('Hello' * 3) 
# Output : HelloHelloHello

print('2' * 3) 
# Output : 222

print('2' + 4) 
# Output : Error: sayı ile string toplanırsa hata verir
```
{% endtab %}

{% tab title="Indexing" %}
```python
text = "Hello World Again"

print(text[0]) # Output : H
print(text[4]) # Output : o

# reverse

print(text[-1]) # Output : n
print(text[-3]) # Output : aprint('Hello' + 'World') 
```
{% endtab %}

{% tab title="Slicing" %}
```python
text = "Hello World Again"

print(text[0:5])    # Hello
print(text[:5])     # Hello
print(text[6:11])   # World
print(text[-11:-6]) # World
print(text[6:-6])   # World
print(text[6:])     # World Again
print(text[1:-1:2]) # el ol gi
print(text[::2])    # HloWrdAan
print(text[::-1])   # niagA dlroW olleH
```
{% endtab %}

{% tab title="Interpolation" %}
```python
name = 'Adam'
surname = 'Smith'
age = 40

text = 'My name is ' + name + ' ' + surname + '. I am '+ str(age) + ' years old.'
print(text)
# Output : My name is Adam Smith. I am 40 years old.

text = 'My name is %s %s. I am %s years old.' % (name, surname, age)
print(text)
# Output : My name is Adam Smith. I am 40 years old.

text = 'My name is {} {}. I am {} years old.'.format(name, surname, age)
print(text)
# Output : My name is Adam Smith. I am 40 years old.

text = f'My name is {name} {surname}. I am {age} years old.'
print(text)
# Output : My name is Adam Smith. I am 40 years old.
```
{% endtab %}

{% tab title="Methods" %}
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
{% endtab %}
{% endtabs %}

```python
```
