# print()

stringler her zaman tırnak içerisinde yazılır

{% code lineNumbers="true" %}
```python
print('Hello World')
print("Hello World")
print(""" Hello World""")
print('''Hello World''')
```
{% endcode %}

```
Output:
----------------------------------------
Hello World
Hello World
Hello World
Hello World
```

sayılar tırnak içerisinde yazılmaz

{% code lineNumbers="true" %}
```python
print(5)
print(2021)
```
{% endcode %}

```
Output:
----------------------------------------
5
2021
```

print() fonksiyonuna birden fazla argüman gönderebiliriz

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube')
print(3,5,6,8)
```
{% endcode %}

```
Output:
----------------------------------------
Hello Word Youtube
3 5 6 8
```

sep parametresi ile gönderilen argümanları birleştirebiliriz. hiç bir şey göndermezsek varsayılan olarak boşluk ile birleştirilir.

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-')
print(3, 5, 6, 8, sep='-')
```
{% endcode %}

```
Output:
----------------------------------------
Hello-Word-Youtube
3-5-6-8
```

end parametresi ile sonuna istediğimiz karakteri ekleyebiliriz. hiç bir şey göndermezsek varsayılan olarak yeni satır eklenir.

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-', end='\n')
print(3, 5, 6, 8, sep='-')
```
{% endcode %}

```
Output:
----------------------------------------
Hello-Word-Youtube
3-5-6-8
```

