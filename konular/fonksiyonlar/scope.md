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
