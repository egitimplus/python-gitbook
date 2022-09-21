# Örnekler

```python
# Shifting a list using slicing
def shift_list(array, s):
    """Shifts the elements of a list to the left or right.
    Args:
    array - the list to shift
    s - the amount to shift the list ('+': right-shift, '-': left-shift)
    Returns:
    shifted_array - the shifted list
    GoalKicker.com – Python® Notes for Professionals 145
    """
    # calculate actual shift amount (e.g., 11 --> 1 if length of the array is 5)
    s %= len(array)

    # reverse the shift direction to be more intuitive
    s *= -1
    
    # shift array with list slicing
    shifted_array = array[s:] + array[:s]
    
    return shifted_array

my_array = [1, 2, 3, 4, 5]

# negative numbers
shift_list(my_array, -7) # Out: [3, 4, 5, 1, 2]

# no shift on numbers equal to the size of the array
shift_list(my_array, 5) # Out: [1, 2, 3, 4, 5]

# works on positive numbers
shift_list(my_array, 3) # Out: [3, 4, 5, 1, 2]
```

```
[3, 4, 5, 1, 2]
[1, 2, 3, 4, 5]
[3, 4, 5, 1, 2]
```

```python
data = 'chandan purohit 22 2000' #assuming data fields of fixed length
name_slice = slice(0,15)
age_slice = slice(16,18)
salary_slice = slice(19,None)

#now we can have more readable slices

print(data[name_slice]) #chandan purohit 
print(data[age_slice]) #'22'
print(data[salary_slice]) #'2000'
```

```
chandan purohit
22
2000
```
