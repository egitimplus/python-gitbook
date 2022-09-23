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


Python'da her şey bir nesnedir. Örneğin, string ve list Python nesneleridir. Sınıf, nesneler oluşturmak için bir plan gibidir. Modüler yapısı nedeniyle OOP teknikleri kullanılarak yazılan kodun bakımı kolaydır. OOP'de kullanılan kapsülleme yaklaşımı ile programlar daha güvenlidir.

## Class (Sınıf)

OOP'deki bir sınıf, nesneler için bir plan gibidir ve OOP kullanarak kendi veri yapınızı geliştirebilirsiniz. Örneğin, çalışanla ilgili ad veya maaş gibi özellikleri izlemek için bir Çalışan sınıfı oluşturabilirsiniz.

Gerçek dünyadaki nesnelerin (objects) özellikleri ve davranışları sınıflara aktarılır. Bu durumların sınıflara aktarılması metodlar yardımıyla olur. Sınıfta tanımlanan metot ve değişkenlere sınıfın üyeleri denir.&#x20;

Özellikler (attributes) isim, soyisim, yaş gibi kullanacağımız bilgileri saklamaktadır.  Davranışlar (methods) ise, kullanıcı kaydı, iki sayısının toplamı gibi bir görevi yerine getiren fonksiyonlardır&#x20;

**Sınıf oluşturma**

Python'da class oluşturmak için class anahtar sözcüğü kullanılır. Sınıf adı, sınıf anahtar sözcüğünü ve ardından iki nokta üst üste işareti izler. Sınıfın gövdesi yeni bir satırda başlar ve class anahtar sözcüğünden bir sekme girintilidir.

```python
class Employee:
    '''This is a docstring. I have created a new class'''
    pass
```

## Objects (Nesne)

Daha önce de söylediğim gibi, bir sınıf, nesneler oluşturmak için bir plan gibidir. Yöntemlerini ve niteliklerini kullanmadan önce bir sınıfın nesnesini oluşturmamız gerekir.

Python'da her şey nesnedir. Tam sayılar, ondalık sayılar, dizeler, sözlükler her şey nesnedir. 12 sayısı bir nesnedir veya "Merhaba Dünya" dizesi bir nesnedir.&#x20;

İçinde veri saklayan ve bu veriler üzerinde işlem yapacak olan metodlar bulunduran bileşenlerdir.  Nesne oluşturduğumuzda hafızada yer kaplar.

**Nesne oluşturma**

Bir nesne aynı zamanda bir örnek olarak da adlandırılır. Bu nedenle, bir sınıfın nesnesini oluşturma işlemine örnekleme denir. Python'da bir sınıfın nesnesini oluşturmak için sınıf adını yazmanız ve ardından parantez açıp kapatmanız gerekir.

```
obj_1 = Dog()
print(type(obj_1) # __main__.Dog
```

Nesnenin türünü kontrol etmek için type yöntemini kullanabilirim. Aşağıdaki örnekte gördüğünüz gibi emre nesnesinin türü bir Çalışan sınıfıdır.

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
```

Bir nesnenin tüm niteliklerini ve yöntemlerini görmek için yerleşik dir() işlevini kullanabilirsiniz. Python'da bazı yerleşik nitelikler ve yöntemler vardır. Aşağıdaki örnek, emre nesnesinin tüm niteliklerini ve yöntemlerini gösterir. Önünde çift alt çizgi bulunan örnekler, yerleşik nitelikler ve yöntemlerdir.

```python
obj_1 = Dog()
print(dir(obj_1))
```

Sınıfın nesnesini kullanarak sınıf ve örnek niteliklerine erişebilir ve bir örnek yöntemini çağırabilirsiniz. Bunu yapmak için, nesne adını, ardından nokta (.) operatörünü ve erişmek veya çağırmak istediğiniz özniteliğin veya yöntemin adını yazmanız gerekir.&#x20;

```python
rich = Dog()
print(rich.name, rich.age) # Rich 5

ja = Dog()
print(ja.name, ja.age) # Rich 5class Dog:
```

```python
class Dog:
    # class attribitues
    species = 'Canis familiaris'
    
class Car:
    # class attributes
    classification = 'Vehicle'

print(Dog.species)    # Canis familiaris

rich = Dog()
print(rich.species)   # Canis familiaris 
```

Sınıf ve örnek öznitelikleri olmak üzere iki tür öznitelik vardır. Sınıf özniteliklerinin değeri tüm nesnelerde aynıdır, ancak örnek özniteliklerinin değeri nesneler arasında değişebilir.&#x20;

Constructur (yapıcı), bir sınıftan bir nesne oluşturduğunuzda varsayılan olarak çağrılan bir yöntemdir. Bir yapıcı oluşturmak için init anahtar kelimesiyle bir yöntem oluşturmalısınız.&#x20;

```python
class Dog:
    # class attribute
    species = 'Canis familiaris'
    
    def __init__(self, name, age):
        pass
```

Örnek öznitelikleri herhangi bir yöntemin içinde, sınıf öznitelikleri ise yöntemlerin dışında bildirilir. Örnek öznitelikleri self anahtar sözcüğü kullanılarak, sınıf öznitelikleri ise yöntem içindeki sınıf adıyla başvurulur.

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

**instance methods**

Metotları kullanarak bir nesnenin fonksiyonlarını uygulayabilirsiniz.

```
class Dog:
    # class attribute
    species = 'Canis familiaris'
    
    def __init__(self, name, age):
        self.name = name  # instance attribute
        self.age = age    # instance attribute
    
    # instance method
    def speak(self):
        # print('hau hau')
        return 'hau hau'

```

**static methods**

Şimdiye kadar yöntemleri çağırmak için bir sınıfın nesnelerini kullandım, ancak doğrudan sınıf adı kullanılarak çağrılabilen statik bir yöntem olan başka bir yöntem türü daha var. Statik yöntemler yalnızca sınıf özelliklerine erişebilir.

```
// Some code
```

##

## inheritance

## polymorphism

## encapsulation

## dunder (magic) methods
