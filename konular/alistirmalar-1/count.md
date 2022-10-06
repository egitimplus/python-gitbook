# Count

```python
def count_items(data):
    new = {}
    for item in data:
        item_lower = item.lower()
        if item_lower in new:
            new[item_lower] = new[item_lower] + 1
        else:
            new[item_lower] = 1
    return new
    
data = ['Banana','Apple', 'Kiwi', 'Cherry', 'kiwi']
print(count_items(data))
# Output : {'banana': 1, 'apple': 1, 'kiwi': 2, 'cherry': 1}
```

```python
from collections import defaultdict

def count_items(data):
    new = defaultdict(int)

    for item in data:
        new[item.lower()] += 1

    return dict(new)

data = ['Banana','Apple', 'Kiwi', 'Cherry', 'kiwi']
print(count_items(data))
# Output : {'banana': 1, 'apple': 1, 'kiwi': 2, 'cherry': 1}
```

{% hint style="info" %}
The Counter() class will return a dictionary of how many times each item appears in an iterable.
{% endhint %}

```python
from collections import Counter

def count_item(value, data):
    count_value = Counter(data).get(value)
    return count_value

print(count_item('Peter', data))
# Output: 1
```

```python
def count_item(value, data):
    count = 0
    for name in data:
        if name.lower() == value.lower():
            count +=1
    return count

print(count_item('Peter', data))
# Output: 2
```

{% hint style="info" %}
Most Repeated Item
{% endhint %}

```python
def most_repeat(data):
    new = {}
    for item in data:
        item_lower = item.lower()
        if item in new:
            new[item_lower] += 1
        else:
            new[item_lower] = 1

    return sorted(new, key=lambda x: x[1], reverse=True)[0]

data = ['new', 'bold', 'apple', 'yes', 'apple', 'bold', 'new', 'apple']
print(most_repeat(data))
# Output: apple
```

{% hint style="info" %}
Bir fonksiyon yazalım bu fonksiyon verilen metindeki kelimelerin kaç harf olduğunu bize sözlük olarak döndürsün. Her kelime sadece bir kez olsun.
{% endhint %}

```python
def word_dict(text):
    word_list = {}
    words = text.split()

    for word in words:
        word_lower = word.lower()
        if word_lower not in word_list:
            word_list[word_lower] = len(word_lower)

    return word_list

word_dict('My name is Alex. Welcome my home.')
```

{% hint style="info" %}
Bir fonksiyon yazalım bu fonksiyon verilen metindeki kelimelerin kaç kez geçtiğini bize sözlük olarak döndürsün.
{% endhint %}

```python
def word_count(text):
    word_list = {}
    words = text.split()

    for word in words:
        word_lower = word.lower()
        if word_lower not in word_list:
            word_list[word_lower] = 1
        else:
            word_list[word_lower] += 1

    return word_list

word_count('My name is Alex. Welcome my home.')
```

{% hint style="info" %}
Bir fonksiyon yazalım bu fonksiyon içerisine gönderilen metinde kaç tane farklı kelime ve harf olduğunu tespit etsin.
{% endhint %}

```python
def count_words_chars(text):
    word_count = len(set(text.split()))
    letter_count = len(set(text.replace(' ', '')))

    return word_count, letter_count

print(count_words_chars('Hello this funcion works!'))
# Output : (4, 16)
```

{% hint style="info" %}
Bir fonksiyon yazalım bu fonksiyon bir cümledeki sesli harfleri bulsun ve bu harflerin sayıları çarpsın

Benim adım emre ya sen? 2 x 2 x 2 x 1 x 1 = 8

Örneği geliştirelim kelime içerisinde büyük harf varsa çarpmasın 2 x 2 x 1 x 1 = 4
{% endhint %}

```python
def multiply_vowels(text):
    vowels = "AaEeIiOoUu"
    words = text.split()

    vowel_multiply = 1
    for word in words:
        vowel_count = 0
        for letter in word:
            if letter in vowels:
                vowel_count += 1
        if vowel_count > 0:
            vowel_multiply *= vowel_count

    return vowel_multiply

print(multiply_vowels('Hello my name is Alexander.'))
# Output: 16
```
