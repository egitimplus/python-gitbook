# break statement

devam eden bir süreci kesintiye uğratmak için kullanılır.

```python
while True:
    username = input('Enter username : ')
    if len(username) < 4:
        print('Username cannot be less than 4 characters')
    else:
        print('Successfully')
        break
        
'''
Enter username : asdsad
Successfully
'''
```
