# Scope

## Global Değişken

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

## Local Değişken

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

## global ifadesi

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

## Örnekler:

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
