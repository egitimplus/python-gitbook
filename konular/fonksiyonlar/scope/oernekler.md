# Örnekler

```python
foo = 1

def func():
    bar = 2
    print(globals().keys()) # prints all variable names in global scope
    print(locals().keys()) # prints all variable names in local scope

func()
```

```
dict_keys(['__name__', '__doc__', '__package__', '__loader__', '__spec__', '__builtin__', '__builtins__', '_ih', '_oh', '_dh', 'In', 'Out', 'get_ipython', 'exit', 'quit', '_', '__', '___', '_i', '_ii', '_iii', '_i1', 'faktoryel', 'i', 'toplam', '_i2', 'baslangic', 'bitis', 'adet', '_i3', '_i4', 'my_function', '_i5', 'x', '_i6', '_i7', 'foo', 'func'])
dict_keys(['bar'])
```

```python
'''
What happens with name clashes?
'''
foo = 1
def func():
    foo = 2 # creates a new variable foo in local scope, global foo is not affected
    print(foo) # prints 2
 
    # global variable foo still exists, unchanged:
    print(globals()['foo']) # prints 1
    print(locals()['foo']) # prints 2

func()
```

```
2
1
2
```

```python
'''
To modify a global variable, use keyword global:
'''
foo = 1
def func():
    global foo
    foo = 2 # this modifies the global foo, rather than creating a local variable
func()
print(foo)
```

```
2
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
```

```
UnboundLocalError: local variable 'foo' referenced before assignment
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
```

```
7
7
7
```
