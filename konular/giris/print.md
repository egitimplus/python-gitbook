# print()

{% hint style="warning" %}
stringler her zaman tırnak içerisinde yazılır
{% endhint %}

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

{% hint style="warning" %}
sayılar tırnak içerisinde yazılmaz
{% endhint %}

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

{% hint style="warning" %}
print() fonksiyonuna birden fazla argüman gönderebiliriz
{% endhint %}

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

{% hint style="warning" %}
sep parametresi ile gönderilen argümanları birleştirebiliriz. hiç bir şey göndermezsek varsayılan olarak boşluk ile birleştirilir.
{% endhint %}

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

{% hint style="warning" %}
end parametresi ile sonuna istediğimiz karakteri ekleyebiliriz. hiç bir şey göndermezsek varsayılan olarak yeni satır eklenir.
{% endhint %}

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

