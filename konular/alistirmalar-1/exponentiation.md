# Exponentiation

```python
import math
import operator

a, b = 4, 3

print((a ** b)) # = 64
print(pow(a, b)) # = 64
print(math.pow(a, b)) # = 64.0
print(operator.pow(a, b)) # = 64

'''
Another difference between the built-in pow and math.pow is that the built-in pow can accept three arguments:
'''
a, b, c = 2, 3, 2
print(pow(2, 3, 2)) # 0, calculates (2 ** 3) % 2

'''
Special functions
The function math.sqrt(x) calculates the square root of x.
'''
print(math.sqrt(a)) # = 2.0 (always float; does not allow complex results)
print(math.pow(a, 1/3)) # evaluates to 2.0
print(a**(1/3)) # evaluates to 2.0

'''
The function math.exp(x) computes e ** x.
'''
print(math.exp(0)) # 1.0
print(math.exp(1)) # 2.718281828459045 (e)

'''
Trigonometri
'''
print(math.cos(0))
print(math.sin(45))

'''
Logaritma
'''
print(math.log(5)) # = 1.6094379124341003
print(math.log(5, math.e)) # = 1.6094379124341003
print(math.log(1000, 10)) # 3.0 (always returns float)
print(math.log10(1000)) # 3.0
print(math.log2(8)) # 3.0
```
