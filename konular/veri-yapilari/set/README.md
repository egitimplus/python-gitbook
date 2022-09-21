# Küme

| İşlem         | Metod                 | Op     |     Inplace Metod    |  Op |
| ------------- | --------------------- | ------ | :------------------: | :-: |
| Kesişim       | intersection          | a & b  | intersection\_update |  &= |
| Birleşim      | union                 | a \| b |        update        | \|= |
| Fark          | difference            | a - b  |  difference\_update  |  -= |
| Simetrik Fark | symmetric\_difference | a ^ b  |                      |     |
| Üst Küme      | issuperset            | >=     |                      |     |
| Alt Küme      | issubset              | <=     |                      |     |
| Ayrık Küme    | isdisjoint            |        |                      |     |

## Kesişim

```
s1 = {1, 2, 3, 4}
s2 = {3, 4, 5}

s3 = s1.intersection(s2) 
s3 = s1 & s2 

s1.intersection_update(s2)

# {3, 4}
```

## Birleşim

```
s3 = s1.union(s2) 
s3 = s1 | s2 

s1.update(s2)

# {1, 2, 3, 4, 5}
```

## Fark

```
s3 = s1.difference(s2) 
s3 = s1 - s2 

s1.difference_update(s2)

# {1, 2}
```

## Simetrik Fark

```
s3 = s1.symmetric_difference(s2) 
s3 = s1 ^ s2 

# {1, 2, 5}
```

## Üst Küme

```
s3 = {1, 2}

s1.issuperset(s3)
s1 >= s3
# True
```

## Alt Küme

```
s3.issubset(s1) 
s3 <= s1
# True
```

## Ayrık Küme

```
s4 = {3, 4}
s3.isdisjoint(s4) 
# True
```

```python


# Existence check
2 in {1,2,3} # True
4 in {1,2,3} # False
4 not in {1,2,3} # True

# Add and Remove
s = {1,2,3}
s.add(4) # s == {1,2,3,4}
s.discard(3) # s == {1,2,4}
s.discard(5) # s == {1,2,4}
s.remove(2) # s == {1,4}
s.remove(2) # KeyError!

'''
Set operations return new sets, but have the corresponding in-place versions:

method          in-place operation       in-place method
---------------------------------------------------------------------
union           -> s |= t                   update
intersection    -> s &= t                   intersection_update
difference      -> v -= t                   difference_update


Method                      Operator
--------------------------------------------
a.intersection(b)               a & b
a.union(b)                      a | b
a.difference(b)                 a - b
a.symmetric_difference(b)       a ^ b
a.issubset(b)                   a <= b
a.issuperset(b)                 a >= b

'''

# Get the unique elements of a list

restaurants = ["McDonald's", "Burger King", "McDonald's", "Chicken Chicken"]
unique_restaurants = set(restaurants)
print(list(unique_restaurants))

# Sets of Sets
{frozenset({1, 2}), frozenset({3, 4})}




```

```
data = [1, 2, 3, 4, 4, 5, 5]
new_set = set()

for item in data:
    if item % 2 == 0:
        new_set.add(item)

print(new_set)

new_set = {item for item in data if item % 2 == 0}

print(new_set)
```
