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
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', 
'__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', 
'__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', 
'__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', 
'__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 
'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 
'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 
'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 
'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 
'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 
'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

sayi = 5
print(dir(sayi))
'''
['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', 
'__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', 
'__format__', '__ge__', '__getattribute__', '__getnewargs__', '__gt__', '__hash__', 
'__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', 
'__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', 
'__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', 
'__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', 
'__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', 
'__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', 
'__xor__', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'numerator', 
'real', 'to_bytes']
'''
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



