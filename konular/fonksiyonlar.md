---
description: Positional Arguments
---

# Fonksiyonlar

## Fonksiyon Tanımlama

```
f(x) = 2x + 5

x -> 3
f(x) = 2 * 3 + 5
f(x) = 11

x -> 5
f(x) = 2 * 5 + 5
f(x) = 15
```

Fonksiyonlar def ile tanımlanır.

```python
def fruit_juicer():
    """
    function description : docstring
    """
    print('I am fruit juicer')
```

## Fonksiyon Yardımı - help()

```python
print(help(len))

'''
Help on built-in function len in module builtins:

len(obj, /)
    Return the number of items in a container.
'''
```

```python
print(help(fruit_juicer))

'''
Help on function fruit_juicer in module __main__:

fruit_juicer()
    function description
'''
```

## Fonksiyon Çağırma

```python
print(fruit_juicer)
# <function fruit_juicer at 0x7f099253fd40>

fruit_juicer()
# I am fruit juicer// Some code
```

## Parametre & Argüman

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

## Return

Fonksiyonlar geriye değer döndürebilir.

```python
def fruit_juicer(fruit):
    return f'I am {fruit} juicer'

juicer = fruit_juicer('apple')
print(juicer) # I am apple juicer
```

```python
def sum(a, b):
    return a + b

result = sum(3, 5)

print(result) # 8
```

```python
def sum_minus(a, b):
    minus = a - by
    sum = a + b
    return sum, minus

result = sum_minus(3, 5)
print(result) # (8, -2)

sum, min = sum_minus(6, 2) 
print(sum, min) # 8 4
```

```python
def function(number):
    if number > 5:
        return True
    else:
        return False

print(function(3)) # False
```

```python
def function(number):
    if number > 5:
        return True
    
    return False

print(function(3)) # False
```

```python
def function(number):   
    return number > 5

print(function(3)) # False
```





## Scope

### Global Değişken

Global değişken fonksiyon içerisinde de çalışır

```python
if 'x' in globals():
    del x

x = 'global_variable'

def my_function():
    print('inside: ', x)

my_function()         # inside:  global_variable
print('outside: ', x) # outside:  global_variable
```

### Local Değişken

Bir değişkeni fonksiyon içerisinde kullanırsan sadece o fonksiyon için geçerli olur.&#x20;

```python
if 'x' in globals():
    del x

def my_function():
    x = 'local variable'
    print('inside: ', x)

my_function()            # inside:  local variable
print('outside: ', x)    # NameError: name 'x' is not defined
```

### global statement

Her zaman kullanmak için global olarak tanımlanması gerekir. Local değişkeni global değişkene çevirebiliriz

```python
if 'x' in globals():
    del x

def my_function():
    global x
    x = 'local variable'
    print('inside: ', x)

my_function()            # inside:  local variable
print('outside: ', x)    # outside:  local variable
```

```python
x = 0

def my_function():
    # x global yaparsak x'e yeni değer atayabiliriz
    global x
    x = x + 1
    print(x)

my_function()   # 1 
print(x)        # 1
```

### Alıştırmalar

```python
foo = 1

def func():
    bar = 2
    print(globals().keys()) # prints all variable names in global scope
    print(locals().keys()) # prints all variable names in local scope

func()

'''
dict_keys(['foo', 'func'])
dict_keys(['bar'])
'''
```

```python
foo = 1
def func():
    foo = 2 # creates a new variable foo in local scope, global foo is not affected
    print(foo) # 2
 
    # global variable foo still exists, unchanged:
    print(globals()['foo']) # 1
    print(locals()['foo']) # 2

func()
# 2
# 1
# 2
```

```python
foo = 1
def func():
    global foo
    foo = 2 # this modifies the global foo, rather than creating a local variable

func()
print(foo) # 2
```

```python
'''
The scope is defined for the whole body of the function!
What it means is that a variable will never be global for a half of the function and local afterwards, or vice-versa.
'''

foo = 1
def func():
    # This function has a local variable foo, because it is defined down below.
    # So, foo is local from this point. Global foo is hidden.
    print(foo) # raises UnboundLocalError, because local foo is not yet initialized
    foo = 7
    print(foo)
    
func()
# UnboundLocalError: local variable 'foo' referenced before assignment
```

```python
foo = 1
def func():
    # In this function, foo is a global variable from the beginning
    global foo
    foo = 7 # global foo is modified
    print(foo) # 7
    print(globals()['foo']) # 7
    print(foo) # 7

func()
# 7
# 7
# 7
```
