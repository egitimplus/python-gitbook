# alıştırmalar

```
Aşağıda adımları verilen programı yapınız

1- Kullanıcıya ismini soralım
2- «Emre» cevabını verene kadar sormaya devam edelim.
3- «Emre» cevabını verdiğinde şifresini soralım.
4- Eğer girilen şifre «gizlişifre» değil ise ismini (1. adım) soralım. Eğer şifre doğru ise ekrana «Giriş Başarılı» yazdıralım.

```

{% hint style="info" %}
Use for, .split(), and if to create a Statement that will print out words that start with 's':
{% endhint %}

```python
st = 'Print only the words that start with s in this sentence'

for word in st.split():
    if word[0] == 's':
        print(word)
        
'''
start
s
sentence
'''
```

{% hint style="info" %}
Use range() to print all the even numbers from 0 to 10.
{% endhint %}

```python
list(range(0,11,2)) # [0, 2, 4, 6, 8, 10]
```

{% hint style="info" %}
Go through the string below and if the length of a word is even print "even!"
{% endhint %}

```python
for word in st.split():
    if len(word)%2 == 0:
        print(word+" <-- has an even length!")
```

{% hint style="info" %}
Write a program that prints the integers from 1 to 100. But for multiples of three print "Fizz" instead of the number, and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".
{% endhint %}

```python
for num in range(1,101):
    if num % 3 == 0 and num % 5 == 0:
        print("FizzBuzz")
    elif num % 3 == 0:
        print("Fizz")
    elif num % 5 == 0:
        print("Buzz")
    else:
        print(num)
```
