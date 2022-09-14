# any & all

<pre class="language-python"><code class="lang-python"># any and all

# You can use all() to determine if all the values in an iterable evaluate to True

nums = [1, 1, 0, 1]
<strong>print(all(nums))
</strong># False

chars = ['a', 'b', 'c', 'd']
print(all(chars))
# True

# Likewise, any() determines if one or more values in an iterable evaluate to True

nums = [1, 1, 0, 1]
<strong>print(any(nums))
</strong># True

vals = [None, None, None, False]
any(vals)
# False

vals = [1, 2, 3, 4]

<strong>print(any(val > 12 for val in vals))
</strong># False

print(any((val * 2) > 6 for val in vals))
# True
</code></pre>

```
False
True
True
False
True
```

```python
# Remove duplicate values in list

names = ["aixk", "duke", "edik", "tofp", "duke"]
print(list(set(names)))

import collections
collections.OrderedDict.fromkeys(names).keys()
```

```
['duke', 'tofp', 'edik', 'aixk']
odict_keys(['aixk', 'duke', 'edik', 'tofp'])
```
