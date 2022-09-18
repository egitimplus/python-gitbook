# Test

### Numbers <a href="#numbers" id="numbers"></a>

{% hint style="info" %}
Write an equation that uses multiplication, division, an exponent, addition, and subtraction that is equal to 100.25.
{% endhint %}

```
# Your answer is probably different
(60 + (10 ** 2) / 4 * 7) - 134.75
```

{% hint style="info" %}
Answer these 3 questions without typing code. Then type code to check your answer.

What is the value of the expression 4 \* (6 + 5)

What is the value of the expression 4 \* 6 + 5

What is the value of the expression 4 + 6 \* 5
{% endhint %}

```
44
29
34
```

{% hint style="info" %}
What is the type of the result of the expression 3 + 1.5 + 4?
{% endhint %}

```
Floating Point Number
```

{% hint style="info" %}
What would you use to find a number’s square root, as well as its square?
{% endhint %}

```
# Square root : 
print(100 ** 0.5)

# Square : 
print(10 ** 2)
```

### Strings <a href="#strings" id="strings"></a>

{% hint style="info" %}
Given the string 'hello' give an index command that returns 'e'.
{% endhint %}

```
s = 'hello'
# Print out 'e' using indexing

s[1] # e
```

{% hint style="info" %}
Reverse the string 'hello' using slicing:
{% endhint %}

```
s ='hello'
# Reverse the string using slicing
```

{% hint style="info" %}
Given the string hello, give two methods of producing the letter 'o' using indexing.
{% endhint %}

```
s ='hello'
# Print out the 'o'

# Method 1:
s[-1] # o

# Method 2:
s[4] # o
```

### Lists <a href="#lists" id="lists"></a>

{% hint style="info" %}
Build this list \[0,0,0] two separate ways.
{% endhint %}

```
# Method 1:
[0] * 3 # [0, 0, 0]

# Method 2:
list2 = [0,0,0]
list2 # [0, 0, 0]
```

{% hint style="info" %}
Reassign 'hello' in this nested list to say 'goodbye' instead:
{% endhint %}

```
list3 = [1,2,[3,4,'hello']]

list3[2][2] = 'goodbye'

list3 # [1, 2, [3, 4, 'goodbye']]
```

{% hint style="info" %}
Sort the list below:
{% endhint %}

```
list4 = [5,3,4,6,1]

# Method 1:
sorted(list4) # [1, 3, 4, 5, 6]

# Method 2:
list4.sort()
list4 # [1, 3, 4, 5, 6]
```

### Dictionaries <a href="#dictionaries" id="dictionaries"></a>

{% hint style="info" %}
Using keys and indexing, grab the 'hello' from the following dictionaries:
{% endhint %}

```
d = {'simple_key':'hello'}
d['simple_key'] # 'hello'

d = {'k1':{'k2':'hello'}}
d['k1']['k2'] # 'hello'

d = {'k1':[{'nest_key':['this is deep',['hello']]}]}
d['k1'][0]['nest_key'][1][0] # 'hello'

d = {'k1':[1,2,{'k2':['this is tricky',{'tough':[1,2,['hello']]}]}]}
d['k1'][2]['k2'][1]['tough'][2][0] # 'hello'
```

{% hint style="info" %}
Can you sort a dictionary? Why or why not?

**Answer: No! Because normal dictionaries are **_**mappings**_** not a sequence.**
{% endhint %}

### Tuples <a href="#tuples" id="tuples"></a>

{% hint style="info" %}
What is the major difference between tuples and lists?&#x20;

**Answer: Tuples are immutable!**
{% endhint %}

{% hint style="info" %}
How do you create a tuple?
{% endhint %}

```
t = (1,2,3)
```

### Sets <a href="#sets" id="sets"></a>

{% hint style="info" %}
What is unique about a set?

**Answer: They don't allow for duplicate items!**
{% endhint %}

{% hint style="info" %}
Use a set to find the unique values of the list below:v
{% endhint %}

```
list5 = [1,2,2,33,4,4,11,22,3,3,2]

set(list5) # {1, 2, 3, 4, 11, 22, 33}
```

### Booleans <a href="#booleans" id="booleans"></a>

{% hint style="info" %}
What will be the resulting Boolean of the following pieces of code
{% endhint %}

```
# Answer before running cell
2 > 3 # False

# Answer before running cell
3 <= 2 # False

# Answer before running cell
3 == 2.0 # False

# Answer before running cell
3.0 == 3 # True

# Answer before running cell
4**0.5 != 2 # False
```

{% hint style="info" %}
What is the boolean output of the cell block below?
{% endhint %}

```
# two nested lists
l_one = [1,2,[3,4]]
l_two = [1,2,{'k1':4}]

# True or False?
l_one[2][0] >= l_two[2]['k1'] # False
```
