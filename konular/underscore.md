# Underscore

## 1. Use in Interpreter <a href="#1.-use-in-interpreter" id="1.-use-in-interpreter"></a>

```python
>>> 5 + 4
9
>>> _     # stores the result of the above expression
9
>>> _ + 6
15
```

2\. Ignoring Values\



```python
## ignoring a value
a, _, b = (1, 2, 3) # a = 1, b = 3
print(a, b)

## ignoring multiple values
## *(variable) used to assign multiple value to a variable as list while unpacking
## it's called "Extended Unpacking", only available in Python 3.x
a, *_, b = (7, 6, 5, 4, 3, 2, 1)
print(a, b)
```

## 3. Use in Looping <a href="#3.-use-in-looping" id="3.-use-in-looping"></a>

```python
## iterating over a list using _
## you can use _ same as a variable
languages = ["Python", "JS", "PHP", "Java"]
for _ in languages:
    print(_)
```

## 4. Separating Digits of Numbers <a href="#4.-separating-digits-of-numbers" id="4.-separating-digits-of-numbers"></a>

```python
## different number systems
## you can also check whether they are correct or not by coverting them into integer using "int" method
million = 1_000_000
binary = 0b_0010
octa = 0o_64
hexa = 0x_23_ab

print(million)
print(binary)
print(octa)
print(hexa)
```

## 5. Naming Using Underscore(\_) <a href="#5.-naming-using-underscore-_" id="5.-naming-using-underscore-_"></a>

### 5.1. \_single\_pre\_underscore <a href="#5.1.-_single_pre_underscore" id="5.1.-_single_pre_underscore"></a>

```python
# Single Pre Underscore is used for internal use. Most of us don't use it because of that reason.

class Test:

    def __init__(self):
        self.name = "datacamp"
        self._num = 7

obj = Test()
print(obj.name)
print(obj._num)
```

```python
# Single pre underscore doesn't stop you from accessing the single pre underscore variable. 
# But, single pre underscore effects the names that are imported from the module.

def func():
    return "datacamp"

def _private_func():
    return 7
```

```python
>>> from my_functions import *
>>> func()
'datacamp'
>>> _private_func()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name '_private_func' is not defined
```

```python
>>> import my_functions
>>> my_functions.func()
'datacamp'
>>> my_functions._private_func()
7
```

### 5.2 single\_post_underscore_ <a href="#5.2-single_postunderscore" id="5.2-single_postunderscore"></a>

```python
# Sometimes if you want to use Python Keywords as a variable, function or class names,
# you can use this convention for that. You can avoid conflicts with the Python Keywords by 
# adding an underscore at the end of the name which you want to use.

>>> def function(class):
  File "<stdin>", line 1
    def function(class):
                 ^
SyntaxError: invalid syntax
>>> def function(class_):
...     pass
...
>>>
```

### 5.3. Double Pre Underscore <a href="#5.3.-double-pre-underscore" id="5.3.-double-pre-underscore"></a>

```python
# Double Pre Underscores are used for the name mangling. Double Pre Underscores tells the Python 
# interpreter to rewrite the attribute name of subclasses to avoid naming conflicts.

# Name Mangling:- interpreter of the Python alters the variable name in a way that it is challenging 
# to clash when the class is inherited.

class Sample():

    def __init__(self):
        self.a = 1
        self._b = 2
        self.__c = 3
obj1 = Sample()
dir(obj1)

'''
['_Sample__c',
'__class__',
...
 '_b',
 'a']
 
 _Sample__c. This is the name mangling. It is to avoid the overriding of the variable in subclasses.
 '''
 
 
 print(obj1.__c) # AttributeError: 'Sample' object has no attribute '__c'
 print(obj1._Sample__c) # 3
 
```

### 5.4. Double Pre And Post Underscores <a href="#5.4.-double-pre-and-post-underscores" id="5.4.-double-pre-and-post-underscores"></a>

```python
# In Python, you will find different names which start and end with the double underscore. They are called as magic methods or dunder methods.

class Sample():

    def __init__(self):
        self.__num__ = 7

obj = Sample()
obj.__num__
```

\
