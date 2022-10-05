# Text

Bir fonksiyon yazalım. BU fonksiyon içerisine gönderilen cümledeki her kelimenin ilk harfini büyük diğerlerini küçük yapsın

```python
def capitalize(text):
    return text.capitalize()

capitalize('this Text sHow')
# Output: 'This text show'
```

```python
def capitalize(text):
    return text[0].upper() + text[1:].lower()


print(capitalize('this Text sHow'))
# Output: 'This text show'
```

Bir fonksiyon yazalım bu fonksiyon bir metindeki boş karakletleri \_ ile değiştirsin.

```python
def replace_whitespace(text):
    return text.replace(' ', '')

print(replace_whitespace('He ll o     World'))
# Output: HelloWorld
```

Bir fonksiyon yazalım. BU fonksiyon içerisine gönderilen cümledeki büyük harfleri küçük, küçük harfleri büyük yapsın

```python
def swapcase(text):
    new_text = ''
    for letter in text:
        if letter.islower():
            new_text += letter.upper()
        else:
            new_text += letter.lower()

    return new_text

print(swapcase('HeLLoWorLD!!-+'))
# Output: hEllOwORld!!-+
```

```python
def swapcase(text):
    return text.swapcase()

print(swapcase('HeLLoWorLD!!-+'))
# Output: hEllOwORld!!-+
```
