# match statement

```python
# python 3.10+
# kodları denemek lazım
x = 2

match x:
    case 1:
        print('x')
    case 2:
        print('y')
    case _:
        print('a')
```

```
y
```

You can combine several literals in a single pattern using `|` (“or”):

```python
case 401 | 403 | 404:
    print("Not allowed")
```

```python
point = (3, 4)

match point:
    case (0, 0):
        print("Origin")
    case _:
        print("Not Origin")
```

```
Not Origin
```

```python
point = (0, 0)
x = 5

match point:
    case (0, 0) if x == 5:
        print("Origin for 5")
    case _:
        print("Not Origin for 5")
```

```
Origin for 5
```

```python
from enum import Enum
class Color(Enum):
    RED = 'red'
    GREEN = 'green'
    BLUE = 'blue'

color = Color(input("Enter color: "))

match color:
    case Color.RED:
        print("I see red!")
    case Color.GREEN:
        print("Grass is green")
    case Color.BLUE:
        print("I'm feeling the blues :(")
```

```
Enter color: red
I see red!
```

\
