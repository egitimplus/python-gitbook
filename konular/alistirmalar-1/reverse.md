# Reverse

{% hint style="info" %}
Listeyi tersine çeviren kodu yazınız
{% endhint %}

```python
data = ['paris', 'istanbul', 'Newyork', 'berlin']

def list_reverse(data):
    new = data.copy()
    new.reverse()

    return new

print(list_reverse(data))
```

```python
def list_reverse(data):
    return data[::-1]

print(list_reverse(data))
```

{% hint style="info" %}
Bir fonksiyon yazalım ve bu fonksiyon parametre olarak girilen sayıların ortalamasını alsın
{% endhint %}

```python
def my_avg(*numbers):
    return sum(numbers) / len(numbers)

my_avg(3,5,7,10) 
```

{% hint style="info" %}
Palindrome
{% endhint %}

```python
def palindrome(word):
    if word == word[::-1]:
        return True

    return False

print(palindrome('kabak'))
# Output: True
```
