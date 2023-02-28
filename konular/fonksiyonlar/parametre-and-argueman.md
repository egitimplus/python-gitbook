---
description: Positional Arguments
---

# parametre & argüman

Fonksiyona girdi olarak kullanılan değişkenlere parametre, fonksiyon çağırılırken gönderilen değerlere argüman denir.

### Pozisyonel Argümanlar

```python
def fruit_juicer(fruit): # name parametre
    print(f'I am {fruit} juicer')

fruit_juicer('orange') 
# I am orange juicer
```

```python
def fruit_juicer(fruit1, fruit2):
    print(f'I am {fruit1} and {fruit2} juicer')

fruit_juicer('orange', 'apple') 
# I am orange and apple juicer
```

```python
def sum(a, b):
    print(a + b)

sum(3, 5) 
# 8
```

### Anahtar Kelimeli Argümanlar

```python
def fruit_juicer(fruit1, fruit2):
    print(f'I am {fruit1} and {fruit2} juicer')

fruit_juicer(fruit1='apple', fruit2='orange') 
# I am apple and orange juicer
```

```python
def parrot(voltage, state='a stiff', action='voom', type='Norwegian Blue'):
    print("-- This parrot wouldn't", action, end=' ')
    print("if you put", voltage, "volts through it.")
    print("-- Lovely plumage, the", type)
    print("-- It's", state, "!")

parrot(1000)                                          # 1 positional argument
parrot(voltage=1000)                                  # 1 keyword argument
parrot(voltage=1000000, action='VOOOOOM')             # 2 keyword arguments
parrot(action='VOOOOOM', voltage=1000000)             # 2 keyword arguments
parrot('a million', 'bereft of life', 'jump')         # 3 positional arguments
parrot('a thousand', state='pushing up the daisies')  # 1 positional, 1 keyword

# but all the following calls would be invalid:

parrot()                     # required argument missing
parrot(voltage=5.0, 'dead')  # non-keyword argument after a keyword argument
parrot(110, voltage=220)     # duplicate value for the same argument
parrot(actor='John Cleese')  # unknown keyword argument
```

### Varsayılan Argümanlı

Fonksiyon tanımlarken parametrelere değer vererek isteğe bağlı hale getirebiliriz.

```python
def fruit_juicer(fruit1, fruit2='orange'):
    print(f'I am {fruit1} and {fruit2} juicer')

fruit_juicer(fruit1='apple')
# I am apple and orange juicer

fruit_juicer(fruit1='apple', fruit2='carrot')
# I am apple and carrot juicer
```

### Değişken Sayılı Argümanlar

#### Pozisyonel

```python
def fruit_juicer(*fruits):
    print(fruits)

    for i in fruits:
        print(i)

fruit_juicer('orange', 'apple', 'carrot')

'''
('orange', 'apple', 'carrot')
orange
apple
carrot
'''
```

#### Anahtar Kelimeli

```python
def fruit_juicer(**kwargs):

    print(kwargs['fruits'])

    size = kwargs.get('size', 'M')
    print(size)

    for k, v in kwargs.items():
        print(k, v)

fruit_juicer(fruits=['orange', 'apple', 'carrot'], sugar=True, size='L')

'''
['orange', 'apple', 'carrot']
L
fruits ['orange', 'apple', 'carrot']
sugar True
size L
'''
```

```python
# Note on Nesting Functions with Optional Arguments

'''
It is possible to nest such functions and the usual convention is to remove the 
items that the code has already handled but if you yare passing down the 
parameters you need to pass optional positional args with a * prefix and
optional keyword args with a ** prefix, otherwise args with be passed as a list 
or tuple and kwargs as a single dictionary. e.g.:
'''
def fn(**kwargs):
    print(kwargs)
    f1(**kwargs)

def f1(**kwargs):
    print((kwargs))

fn(a=1, b=2)

'''
{'a': 1, 'b': 2}
{'a': 1, 'b': 2}
'''
```

#### Karışık

```python
def fruit_juicer(brand, *args, **kwargs):
    print(brand)
    print(args)
    print(kwargs)

fruit_juicer('XTech', 'orange', 'apple', 'carrot', sugar=True, size='L')

'''
XTech
('orange', 'apple', 'carrot')
{'sugar': True, 'size': 'L'}
'''
```

### Özel Argümanlar

where `/` and `*` are optional. If used, these symbols indicate the kind of parameter by how the arguments may be passed to the function: positional-only, positional-or-keyword, and keyword-only. Keyword parameters are also referred to as named parameters.

```
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
      -----------    ----------     ----------
        |             |                  |
        |        Positional or keyword   |
        |                                - Keyword only
         -- Positional only
```

**Positional-or-Keyword Arguments**

If `/` and `*` are not present in the function definition, arguments may be passed to a function by position or by keyword.

**Positional-Only Arguments**

Looking at this in a bit more detail, it is possible to mark certain parameters as _positional-only_. If _positional-only_, the parameters’ order matters, and the parameters cannot be passed by keyword. Positional-only parameters are placed before a `/` (forward-slash). The `/` is used to logically separate the positional-only parameters from the rest of the parameters. If there is no `/` in the function definition, there are no positional-only parameters. Parameters following the `/` may be _positional-or-keyword_ or _keyword-only_.

**Keyword-Only Arguments**

To mark parameters as _keyword-only_, indicating the parameters must be passed by keyword argument, place an `*` in the arguments list just before the first _keyword-only_ parameter.

```python
def standard_arg(arg):
    print(arg)

standard_arg(2)     # 2
standard_arg(arg=2) # 2
```

```python
def pos_only_arg(arg, /):
    print(arg)
    
pos_only_arg(arg=1)
# TypeError: pos_only_arg() got some positional-only arguments passed as keyword arguments: 'arg'
```

```python
def kwd_only_arg(*, arg):
    print(arg)
    
kwd_only_arg(3)
# TypeError: kwd_only_arg() takes 0 positional arguments but 1 was given

kwd_only_arg(arg=3)
# 3
```

```python
def combined_example(pos_only, /, standard, *, kwd_only):
    print(pos_only, standard, kwd_only)
    
combined_example(1, 2, 3)
# TypeError: combined_example() takes 2 positional arguments but 3 were given

combined_example(1, 2, kwd_only=3)
# 1 2 3

combined_example(1, standard=2, kwd_only=3)
# 1 2 3

combined_example(pos_only=1, standard=2, kwd_only=3)
# TypeError: combined_example() got some positional-only arguments passed as keyword arguments: 'pos_only'
```

Finally, consider this function definition which has a potential collision between the positional argument `name` and `**kwds` which has `name` as a key:

```python
def foo(name, **kwds):
    return 'name' in kwds
    
foo(1, **{'name': 2})
# TypeError: foo() got multiple values for argument 'name'
```

But using `/` (positional only arguments), it is possible since it allows `name` as a positional argument and `'name'` as a key in the keyword arguments:

```python
def foo(name, /, **kwds):
    return 'name' in kwds
    
foo(1, **{'name': 2})
# True
```
