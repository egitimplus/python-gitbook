# Örnekler

{% hint style="warning" %}
```
Sayının pozitif olup/olmadığını bulan programı yazınız.
```
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

```
Output:
----------------------------------------
Please enter number: -8
-8
pozitif sayı değil
```

{% hint style="warning" %}
```
vize ve final sınav notlarından öğrencinin sınıfı geçip geçmediğini 
tespit eden programı yazınız.

passing_grade: 50
midtern_coefficient : %30
final_coefficient: %70
```
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
    print('Failed')h
```

```
Output:
----------------------------------------
Please enter midtern exam: 40
Please enter final exam: 60
Result:  54.0
Passed
```

{% hint style="warning" %}
```
Kullanıcı tarafından girilen sınav puanını nota çeviren programı yazınız. 
Eğer girilen puan 0-100 aralığında değilse ekrana hata mesajı basınız.

  -20  | E
21-40  | D
41-60  | C
61-80  | B
81+    | A
```
{% endhint %}

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

```
Output:
----------------------------------------
Please enter exam grade: 65
B
```
