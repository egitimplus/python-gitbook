# Merhaba Dünya

## etkileşimli kabuk (shell)

stringler her zaman tırnak içerisinde yazılır

{% code lineNumbers="true" %}
```python
'Hello World'        # Hello World    
"Hello World"        # Hello World
""" Hello World"""   # Hello World
'''Hello World'''    # Hello World
```
{% endcode %}

sayılar tırnak içerisinde yazılmaz

{% code lineNumbers="true" %}
```python
5    # 5
2021 # 2021
```
{% endcode %}

## print fonksiyonu

print() fonksiyonuna birden fazla argüman gönderebiliriz

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube') # Hello Word Youtube
print(3,5,6,8) # 3 5 6 8
```
{% endcode %}

## sep parametresi

sep parametresi ile gönderilen argümanları birleştirebiliriz. hiç bir şey göndermezsek varsayılan olarak boşluk ile birleştirilir.

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-') # Hello-Word-Youtube
print(3, 5, 6, 8, sep='-') # 3-5-6-8
```
{% endcode %}

## end parametresi

end parametresi ile sonuna istediğimiz karakteri ekleyebiliriz. hiç bir şey göndermezsek varsayılan olarak yeni satır eklenir.

{% code lineNumbers="true" %}
```python
print('Hello', 'Word', 'Youtube', sep='-', end='\n') # Hello-Word-Youtube
print(3, 5, 6, 8, sep='-', end='!') # 3-5-6-8!
```
{% endcode %}

