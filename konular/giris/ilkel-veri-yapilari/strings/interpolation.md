# Interpolation

```python
name = 'Adam'
surname = 'Smith'
age = 40

text = 'My name is ' + name + ' ' + surname + '. I am '+ str(age) + ' years old.'
print(text)

text = 'My name is %s %s. I am %s years old.' % (name, surname, age)
print(text)

text = 'My name is {} {}. I am {} years old.'.format(name, surname, age)
print(text)

text = f'My name is {name} {surname}. I am {age} years old.'
print(text)
```

```
My name is Adam Smith. I am 40 years old.
My name is Adam Smith. I am 40 years old.
My name is Adam Smith. I am 40 years old.
My name is Adam Smith. I am 40 years old.
```
