---
description: Special Arguments
---

# Özel Argümanlar

where `/` and `*` are optional. If used, these symbols indicate the kind of parameter by how the arguments may be passed to the function: positional-only, positional-or-keyword, and keyword-only. Keyword parameters are also referred to as named parameters.

```
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
      -----------    ----------     ----------
        |             |                  |
        |        Positional or keyword   |
        |                                - Keyword only
         -- Positional only
```

**Positional-or-Keyword Arguments**

If `/` and `*` are not present in the function definition, arguments may be passed to a function by position or by keyword.

**Positional-Only Arguments**

Looking at this in a bit more detail, it is possible to mark certain parameters as _positional-only_. If _positional-only_, the parameters’ order matters, and the parameters cannot be passed by keyword. Positional-only parameters are placed before a `/` (forward-slash). The `/` is used to logically separate the positional-only parameters from the rest of the parameters. If there is no `/` in the function definition, there are no positional-only parameters. Parameters following the `/` may be _positional-or-keyword_ or _keyword-only_.

**Keyword-Only Arguments**

To mark parameters as _keyword-only_, indicating the parameters must be passed by keyword argument, place an `*` in the arguments list just before the first _keyword-only_ parameter.

```python
def standard_arg(arg):
    print(arg)

standard_arg(2)
standard_arg(arg=2)

# 2
# 2

```

```python
def pos_only_arg(arg, /):
    print(arg)
    
pos_only_arg(arg=1)
# TypeError: pos_only_arg() got some positional-only arguments passed as keyword arguments: 'arg'
```

```python
def kwd_only_arg(*, arg):
    print(arg)
    
kwd_only_arg(3)
# TypeError: kwd_only_arg() takes 0 positional arguments but 1 was given

kwd_only_arg(arg=3)
# 3
```

```python
def combined_example(pos_only, /, standard, *, kwd_only):
    print(pos_only, standard, kwd_only)
    
combined_example(1, 2, 3)
# TypeError: combined_example() takes 2 positional arguments but 3 were given

combined_example(1, 2, kwd_only=3)
# 1 2 3

combined_example(1, standard=2, kwd_only=3)
# 1 2 3

combined_example(pos_only=1, standard=2, kwd_only=3)
# TypeError: combined_example() got some positional-only arguments passed as keyword arguments: 'pos_only'
```

Finally, consider this function definition which has a potential collision between the positional argument `name` and `**kwds` which has `name` as a key:

```python
def foo(name, **kwds):
    return 'name' in kwds
    
foo(1, **{'name': 2})
# TypeError: foo() got multiple values for argument 'name'
```

But using `/` (positional only arguments), it is possible since it allows `name` as a positional argument and `'name'` as a key in the keyword arguments:

```python
def foo(name, /, **kwds):
    return 'name' in kwds
    
foo(1, **{'name': 2})
# True
```
