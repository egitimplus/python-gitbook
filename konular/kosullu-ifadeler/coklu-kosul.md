# Çoklu Koşul

```python
//'''
Testing for multiple conditions
A common mistake when checking for multiple conditions is to apply the logic incorrectly.
This example is trying to check if two variables are each greater than 2. The statement is evaluated as - if (a) and
(b > 2). This produces an unexpected result because bool(a) evaluates as True when a is not zero.
'''

a = 1
b = 6

if a and b > 2:
    print('yes')
else:
    print('no')
 

'''
Each variable needs to be compared separately.
'''
if a > 2 and b > 2:
    print('yes')
else:
    print('no')
 
# no

'''
Another, similar, mistake is made when checking if a variable is one of multiple values. The statement in this
example is evaluated as - if (a == 3) or (4) or (6). This produces an unexpected result because bool(4) and
bool(6) each evaluate to True
'''

if a == 3 or 4 or 6:
    print('yes')
else:
    print('no')

# yes

'''
Again each comparison must be made separately
'''
if a == 3 or a == 4 or a == 6:
    print('yes')
else:
    print('no')
 
# no

'''
Using the in operator is the canonical way to write this.
'''

if a in (3, 4, 6):
    print('yes')
else:
    print('no')
    
# no
```

```
Output:
----------------------------------------
yes
no
yes
no
no
```
