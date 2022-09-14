# Karışık

```python
def fruit_juicer(brand, *args, **kwargs):
    print(brand)
    print(args)
    print(kwargs)


fruit_juicer('XTech', 'orange', 'apple', 'carrot', sugar=True, size='L')
```

```
XTech
('orange', 'apple', 'carrot')
{'sugar': True, 'size': 'L'}
```
