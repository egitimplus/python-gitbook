---
description: Variable Number of Arguments
---

# Pozisyonel

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
