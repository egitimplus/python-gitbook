# Anahtar Kelimeli

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
items that the code has already handled but if you are passing down the 
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

```
```
