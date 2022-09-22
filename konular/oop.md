# OOP

Nesne yönelikli programlamaya örnek verecek olursak gerçek hayatta gördüğümüz araba, radyo, bina… gibi nesnelerin bilgisayar ortamına aktarılmasına denir.

Nesne Yönelimli Programlamada 4 temel özellik vardır. Bu özelliklerden birini sağlamayan programlama dili nesne yönelimli programlama dili olarak sayılmaz.

1.) Soyutlama (Abstraction)\
2.) Kapsülleme (Encapsulation)\
3.) Miras Alma (Inheritance)\
4.) Çok biçimlilik (Polymorphism)

**Soyutlama:** Bir sınıfta davranış ve özelliklerin tanımlanmasına soyutlama diyoruz.

**Kapsülleme:** Davranış ve özellikler sınıfta soyutlanarak kapsüllenir. Kapsülleme ile hangi özellik ve davranışın dışarıya sunulup sunulmayacağını belirleriz.

**Kalıtım:** Sınıflar birbirinden türeyebilir. Alt sınıf üst sınıfın özelliklerini alabilir.

**Çok Biçimlilik:** Alt sınıflar üst sınıfın gösterdiği davranışları göstermek zorunda değildir. Alt sınıfların farklı davranışları göstermesine Çok biçimlilik denilmektedir.\


## Class (Sınıf)

Gerçek dünyadaki nesnelerin (objects) özellikleri ve davranışları sınıflara aktarılır. Bu durumların sınıflara aktarılması metodlar yardımıyla olur. Sınıfta tanımlanan metot ve değişkenlere sınıfın üyeleri denir.&#x20;

Özellikler (attributes) isim, soyisim, yaş gibi kullanacağımız bilgileri saklamaktadır.  Davranışlar (methods) ise, kullanıcı kaydı, iki sayısının toplamı gibi bir görevi yerine getiren fonksiyonlardır&#x20;

**Sınıf oluşturma**

```python
class Employee:
    '''This is a docstring. I have created a new class'''
    pass
```

## Objects (Nesne)

Nesne oluşturma

Python'da her şey nesnedir. Tam sayılar, ondalık sayılar, dizeler, sözlükler her şey nesnedir. 12 sayısı bir nesnedir veya "Merhaba Dünya" dizesi bir nesnedir.&#x20;

İçinde veri saklayan ve bu veriler üzerinde işlem yapacak olan metodlar bulunduran bileşenlerdir.  Nesne oluşturduğumuzda hafızada yer kaplar.

Nesnelerimizin hafızada tuttuklerı adresler farkı

```python
print(Dog()) # <__main__.Dog object at 0x106702d30>
print(Dog()) # <__main__.Dog object at 0x0004ccc90>
```

Nesneleri değişkene atadığımızda&#x20;

```python
obj_1 = Dog()
obj_2 = Dog()

print(obj_1 == obj_2) # False
```

obj\_1 ve obj\_2 Dog() sınıfının örnekleri olsa da bellekte iki farklı nesneyi temsil ederler. Oluşturduğumuz nesneye instance'da denir. Sınıfın örnekleri!

## Attributes (Özellikler)

Sınıflarımızın özellikleri olur. Dog sınıfını düşünürsek bunlar ne olabilir ? ismi, yaşı özelliklerine örnek verilebilir.

```python
class Dog:
    name = 'Rich'
    age = 5
    
rich = Dog()
print(rich.name, rich.age) # Rich 5

ja = Dog()
print(ja .name, ja.age) # Rich 5

```

```python
class Dog:
    # class attribitues
    species = 'Canis familiaris'
    
class Car:
    # class attributes
    classification = 'Vehicle'
```

```python
class Dog:
    # class attribute
    species = 'Canis familiaris'
    
    def __init__(self, name, age):
        self.name = name  # instance attribute
        self.age = age    # instance attribute
        

rich = Dog(name='Rich', age=5)
print(rich.name, rich.age) # Rich 5

ja = Dog(name='Ja', age=3)
print(ja.name, ja.age) # Ja 3
```

## Methods (Davranışlar)

## inheritance

## polymorphism

## encapsulation

## dunder (magic) methods
