# Küme

| İşlem         | Metod                 | x      |     Inplace Metod    |  x  |
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
{1, 2, 3, 4, 5}.intersection({3, 4, 5, 6}) 
{1, 2, 3, 4, 5} & {3, 4, 5, 6} 
# {3, 4, 5}
```

## Birleşim

```
{1, 2, 3, 4, 5}.union({3, 4, 5, 6}) 
{1, 2, 3, 4, 5} | {3, 4, 5, 6} 
# {1, 2, 3, 4, 5, 6}
```

## Fark

```
{1, 2, 3, 4}.difference({2, 3, 5}) 
{1, 2, 3, 4} - {2, 3, 5} 
# {1, 4}
```

## Simetrik Fark

```
{1, 2, 3, 4}.symmetric_difference({2, 3, 5}) 
{1, 2, 3, 4} ^ {2, 3, 5} 
# {1, 4, 5}
```

## Üst Küme

```
{1, 2}.issuperset({1, 2, 3})
{1, 2} >= {1, 2, 3} 
# False
```

## Alt Küme

```
{1, 2}.issubset({1, 2, 3}) 
{1, 2} <= {1, 2, 3}
# True
```

## Ayrık Küme

```
{1, 2}.isdisjoint({3, 4}) # True
{1, 2}.isdisjoint({1, 4}) # False
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
