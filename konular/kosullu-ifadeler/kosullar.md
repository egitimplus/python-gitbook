# koşullar

## if

{% hint style="info" %}
```
if <condition>:
    ...
    ...
```
{% endhint %}

```python
if True:
    print('condition is true')
```

```python
x = 4
if x > 5:
    print('x is greater than 5')
```

{% hint style="info" %}
Klavyeden girilen sayı pozitif ise ekrana pozitif yazdırınız
{% endhint %}

```python
number = int(input('Please enter a number'))
if number > 0:
    print('Entered number is positive')
```

## else

{% hint style="info" %}
```
if <condition>:
    ...
    ...
else:
    ...
    ...
```
{% endhint %}

```python
x = 3
if x > 5:
    print('x is greater than 5')
else:
    print('x is less than 5')
```

{% hint style="info" %}
Sayının pozitif olup/olmadığını bulan programı yazınız.
{% endhint %}

```python
number = int(input('Please enter number: '))

print(number)

if number > 0:
    print('pozitif bir sayı')
elif number == 0:
    print('sayı sıfırdır yani nötr')
else:
    print('pozitif sayı değil')
```

{% hint style="info" %}
Klavyeden girilen vize ve final sınav notlarından öğrencinin sınıfı geçip geçmediğini tespit eden programı yazınız.&#x20;

Geçme notu : 50&#x20;

Vize katsayısı : %30&#x20;

Final katsayısı: %70
{% endhint %}

```python
passing_grade = 50
midtern_coef = 0.3
final_coef = 0.7

midterm_exam = input('Please enter midtern exam: ')
final_exam = input('Please enter final exam: ')

result = int(midterm_exam) * midtern_coef + int(final_exam) * final_coef

print('Result: ', result)

if result > passing_grade:
    print('Passed')
else:
    print('Failed')
```

## elif

{% hint style="info" %}
```
if <condition>:
    ...
    ...
elif <condition>:
    ...
    ...
else:
    ...
    ...
```
{% endhint %}

```python
x = 4
if x > 5:
    print('x is greater than 5')
elif x > 3:
    print('x is greater than 3')
else:
    print('x is less than 5')
```

{% hint style="info" %}
Kullanıcı tarafından girilen sınav puanını nota çeviren programı yazınız. Eğer girilen puan 0-100 aralığında değilse ekrana hata mesajı basınız.
{% endhint %}

<table><thead><tr><th width="203">Sınav Puanı</th><th>Not</th></tr></thead><tbody><tr><td>0-20</td><td>E</td></tr><tr><td>21-40</td><td>D</td></tr><tr><td>41-60</td><td>C</td></tr><tr><td>61-80</td><td>B</td></tr><tr><td>81-100</td><td>A</td></tr></tbody></table>

```python
exam_grade = int(input('Please enter exam grade: '))

if exam_grade <= 20:
    print('E')
elif 20 < exam_grade <=40:
    print('D')
elif 40 < exam_grade <= 60:
    print('C')
elif 60 < exam_grade <= 80:
    print('B')
else:
    print('A')
```

## tek satırda if-else

```python
n = 5
result = "Hello" if n > 10 else "Goodbye" if n > 5 else "Good day"
print(result) # Output: Goodbye
```

## çoklu koşul

{% hint style="info" %}
Her değişken ayrı ayrı karşılaştırılmalı.
{% endhint %}

```python
a = 1
b = 6

# Yanlış
if a and b > 2:
    print('yes')
else:
    print('no')

# Output: yes
    
# Doğru    
if a > 2 and b > 2:
    print('yes')
else:
    print('no')
 
# Output: no


```

```python
# Yanlış
if a == 3 or 4 or 6:
    print('yes')
else:
    print('no')
    
# Output : yes

# Doğru
if a == 3 or a == 4 or a == 6:
    print('yes')
else:
    print('no')
 
# Output : no

# Doğru
if a in (3, 4, 6):
    print('yes')
else:
    print('no')

# Output : no
```

## pass ifadesi

```python
if 5 > 3:
    pass
```
