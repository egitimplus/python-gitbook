# print()

{% hint style="info" %}
stringler her zaman tırnak içerisinde yazılır
{% endhint %}

{% code lineNumbers="true" %}
```python
print('Hello World')        # Hello World    
print("Hello World")        # Hello World
print(""" Hello World""")   # Hello World
print('''Hello World''')    # Hello World
```
{% endcode %}

{% hint style="info" %}
sayılar tırnak içerisinde yazılmaz
{% endhint %}

{% code lineNumbers="true" %}
```python
print(5)    # 5
print(2021) # 2021
```
{% endcode %}

{% hint style="info" %}
print() fonksiyonuna birden fazla argüman gönderebiliriz
{% endhint %}

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube') # Hello Word Youtube
print(3,5,6,8) # 3 5 6 8
```
{% endcode %}

{% hint style="info" %}
sep parametresi ile gönderilen argümanları birleştirebiliriz. hiç bir şey göndermezsek varsayılan olarak boşluk ile birleştirilir.
{% endhint %}

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-') # Hello-Word-Youtube
print(3, 5, 6, 8, sep='-') # 3-5-6-8
```
{% endcode %}

{% hint style="info" %}
end parametresi ile sonuna istediğimiz karakteri ekleyebiliriz. hiç bir şey göndermezsek varsayılan olarak yeni satır eklenir.
{% endhint %}

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-', end='\n') # Hello-Word-Youtube
print(3, 5, 6, 8, sep='-', end='!') # 3-5-6-8!
```
{% endcode %}

