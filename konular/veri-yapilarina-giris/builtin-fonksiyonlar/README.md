# builtin fonksiyonlar

## type()

type() fonksiyonu içine yazılan değişkenin veya ifadenin veri tipini dönderir.

```python
number = 5
print(type(number)) # <class 'int'>

print(type(5))      # <class 'int'>

number = 5.0
print(type(number)) # <class 'float'>

string = 'hello'
print(type(string )) # <class 'str'>len()
```

## len()

len() fonksiyonu içerisine gönderilen ifadenin uzunluğunu dönderir.

```python
text = '24123213'
print(len(text))   # 8

number = 24123213
print(len(number)) # TypeError: object of type 'int' has no len()
```

## dir()

```python
print(dir('Hello'))

sayi = 5
print(dir(sayi))
```

```python
print(dir(__builtins__))

'''
['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 
 ...
'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']
'''
```

## input()

Kullanıcıdan veri/bilgi almak için kullanılır. Kullanıcının girdiği veriler her zaman string olarak döner.



