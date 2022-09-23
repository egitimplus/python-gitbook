# OOP

Nesne tabanlı programlama bir yazılım geliştirme yöntemidir. Nesne yönelikli programlamaya örnek verecek olursak gerçek hayatta gördüğümüz araba, radyo, bina… gibi nesnelerin bilgisayar ortamına aktarılmasına denir.

Python'da her şey bir nesnedir. Örneğin, string ve list Python nesneleridir. Sınıf, nesneler oluşturmak için bir plan gibidir.&#x20;

## Class (Sınıf)

OOP'deki bir sınıf, nesneler için bir plan gibidir ve OOP kullanarak kendi veri yapınızı geliştirebilirsiniz. Örneğin, çalışanla ilgili ad veya maaş gibi özellikleri izlemek için bir Çalışan sınıfı oluşturabilirsiniz.

Gerçek dünyadaki nesnelerin (objects) özellikleri ve davranışları sınıflara aktarılır. Bu durumların sınıflara aktarılması metodlar yardımıyla olur. Sınıfta tanımlanan metot ve değişkenlere sınıfın üyeleri denir.&#x20;

Özellikler (attributes) isim, soyisim, yaş gibi kullanacağımız bilgileri saklamaktadır.  Davranışlar (methods) ise, kullanıcı kaydı, iki sayısının toplamı gibi bir görevi yerine getiren fonksiyonlardır&#x20;

**Sınıf oluşturma**

Python'da class oluşturmak için class anahtar sözcüğü kullanılır. Sınıf adı, sınıf anahtar sözcüğünü ve ardından iki nokta üst üste işareti izler. Sınıfın gövdesi yeni bir satırda başlar ve class anahtar sözcüğünden bir sekme girintilidir.

```python
class Car:
    '''This is a docstring. I have created a new class'''
    pass
    
class Dog:
    pass
```

## Objects (Nesne)

Daha önce de söylediğim gibi, bir sınıf, nesneler oluşturmak için bir plan gibidir. Yöntemlerini ve niteliklerini kullanmadan önce bir sınıfın nesnesini oluşturmamız gerekir.

Python'da her şey nesnedir. Tam sayılar, ondalık sayılar, dizeler, sözlükler her şey nesnedir. 12 sayısı bir nesnedir veya "Merhaba Dünya" dizesi bir nesnedir.&#x20;

**Nesne oluşturma**

Bizim oluşturduğumuz Dog_()_ sınıfı bir genel kavram. Şöyle anlatalım bütün köpekler bir yaşı, boyu veya bir rengi var. Yani genel bir sınıflandırma yapıyoruz. Ama siz bu köpeğin rengini, yaşını, boyunu bilemezsiniz. Çünkü _Dog()_ sınıfı bir soyut kavram. Bu yüzden soyut bir kavramın özelliklerini bilemezsiniz. Ama eğer yaşı 25, rengi beyaz gibi özelliklerini belirttiğiniz zaman siz o sınıfı somutlaştırmış bir nesne(object) oluşturmuş olursunuz.

Bir nesne aynı zamanda bir örnek olarak da adlandırılır. Bu nedenle, bir sınıfın nesnesini oluşturma işlemine örnekleme denir. Python'da bir sınıfın nesnesini oluşturmak için sınıf adını yazmanız ve ardından parantez açıp kapatmanız gerekir.

```python
obj_1 = Dog()

obj_1.age = 25
obj_1.color = 'white'
```

Nesnenin türünü kontrol etmek için type yöntemini kullanabilirim. Aşağıdaki örnekte gördüğünüz gibi emre nesnesinin türü bir Dog sınıfıdır.

```
print(type(obj_1) # __main__.Dog
```

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

```python
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

rich = Dog(name='Rich', age=5)
print(rich.speak())  # hau hau
```

```python
class Dog:
    # class attribute
    species = 'Canis familiaris'
    
    def __init__(self, name, age):
        self.name = name  # instance attribute
        self.age = age    # instance attribute
    
    # instance method
    def speak(self, times=2):
        return ' '.join(['hau' for t in range(times)])
 
rich = Dog(name='Rich', age=5)
print(rich.speak(3))  # hau hau hau
```

**static methods**

Şimdiye kadar yöntemleri çağırmak için bir sınıfın nesnelerini kullandım, ancak doğrudan sınıf adı kullanılarak çağrılabilen statik bir yöntem olan başka bir yöntem türü daha var. Statik yöntemler yalnızca sınıf özelliklerine erişebilir.

```python
class Dog:
    # class attribute
    species = 'Canis familiaris'
    
    @staticmethod
    def get_static_method():
        message = "This is static methods. Dont have self parameter"
        print (message)
        
Dog.get_static_method() # This is static methods. Dont have self parameter

rich = Dog()
rich.get_static_method() # This is static methods. Dont have self parame
```

**class methods**

```
// Some code
```

**global & local**

Bir sınıfın niteliklerine de değişkenler denir. İki tür değişken vardır: yerel ve küresel. Bir sınıftaki yerel değişkenler, yalnızca tanımlandığı yöntemin içinden erişilebilen değişkenlerdir. Bu nedenle, get\_static\_method() yönteminin içindeki bir mesaj değişkenine erişemezsiniz. Erişmeye çalıştığınızda aşağıdaki örnekte görüldüğü gibi AttributeError veriyor.

```python
rich = Dog()
rich.message # AttributeError: 'Dog' object has no attribute 'message'
```

Global değişkenler herhangi bir metodun dışında tanımlanır ve herhangi bir yerden erişilebilirler.

```
rich.species # Canis familiaris
```

## Encapsulation (Kapsülleme)

Kapsülleme, veri gizleme anlamına gelir. OOP'de, bir sınıfın diğer sınıfın verilerine doğrudan erişimi olmamalı veya erişim kontrol edilmelidir. Sınıf verilerine erişimi kontrol etmek için özel (private) değişkenleri ve özellikleri kullanabilirsiniz.&#x20;

yaş değişkenine ulaşabiliyor ve değiştirebiliyoruz.&#x20;

```python
class Dog:
    
    def __init__(self, name, age):
        self.name = name  # instance attribute
        self.age = age    # instance attribute


rich = Dog(name='Rich', age=5)
print(rich.age) # 5

rich.age = 15
print(rich.age) # 15
```

Private (özel) bir değişken tanımlamak için değişken adının önüne iki alt çizgi koyabilirsiniz. Örneğin, \_\_age özel bir değişkendir. Yaş değişkenine ulaşmak istediğimizde hata ile karşılaştık. Artık bu değişkenlere sadece sınıf içerisinden ulaşılabilir.

```python
class Dog:
    
    def __init__(self, name, age):
        self.__name = name  # instance attribute
        self.__age = age    # instance attribute
        
rich = Dog(name='Rich', age=5)

print(rich.age) # AttributeError: 'Dog' object has no attribute 'age'
```

Peki ben değer güncellemek istemiyorum ama okumak istiyorsam ne yapacağım ?

```python
class Dog:
    
    def __init__(self, name, age):
        self.__name = name  # instance attribute
        self.__age = age    # instance attribute
    
    def get_age(self):
        return self.__age
        
rich = Dog(name='Rich', age=5)
print(rich.get_age()) # 5
```

Şimdi buna birde güncelleme için bir metod ekleyelim.

```python
class Dog:
    
    def __init__(self, name, age):
        self.__name = name  # instance attribute
        self.__age = age    # instance attribute
    
    def get_age(self):
        return self.__age
    
    def set_age(self, age):
        self.__age = age
        
rich = Dog(name='Rich', age=5)
rich.set_age(15)
print(rich.get_age()) # 15
```

setage kullandığımda değiştirebiliyorum. Böyle bir method kullanmamıza ne gerek vardı ? Çünkü daha öncesinde hiç bir kontrol yapmadan değişkeni değiştirebiliyordum. set\_age metodu ile birlikte artık değişiklik oldugunda log tutabilirim veya öncesinde validasyona tabi tutabilirim. Örnekte de görüldüğü gibi 20'den yüksek yaş girildiğinde artık kabul etmiyoruz.

```python
class Dog:
    
    def __init__(self, name, age):
        self.__name = name  # instance attribute
        self.__age = age    # instance attribute
    
    def get_age(self):
        return self.__age
    
    def set_age(self, age):
        if age > 20:
            raise ValueError('Your dog age is too old')
        self.__age = age
        
rich = Dog(name='Rich', age=5)
rich.set_age(15)
print(rich.get_age()) # 15
```

## Inheritance (Kalıtım)

OOP'deki kalıtım, bir çocuğun kendi benzersiz özelliklerine ek olarak ebeveynlerinden bazı özellikleri miras aldığı gerçek dünya mirasına benzer. Başka bir sınıfı miras alan sınıfa alt sınıf, başka bir sınıf tarafından miras alınan sınıfa ise üst sınıf denir. Aşağıdaki kod, bir kalıtım örneği gösterir. Bir sınıfı miras almak için, alt sınıf adından sonra gelen parantez içine üst sınıf adını yazmalısınız.&#x20;

```python
# Create Class ShepherdDog that inherits Dog
class ShepherdDog(Dog):
    pass
```

ShepherdDog sınıfı, aşağıdaki örnekte gösterildiği gibi, ana Dog sınıfının tüm özniteliklerine ve yöntemlerine erişebilir.

```python
k9= ShepherdDog(name='K9', 3)

print(k9.name) # K9
```

ShepherdDog sınıfının, Dog sınıfının yöntem ve niteliklerine ek olarak kendi özellik ve yöntemleri de olabilir.&#x20;

```python
class ShepherdDog(Dog):
    
    def certificate(self):
        return 'method for shepherd dogs'
        
k9= ShepherdDog(name='K9', 3)

print(k9.certificate()) # method for shepherd dogs
```

### Method overriding

Yöntem geçersiz kılma, alt sınıfta üst sınıfta olduğu gibi aynı ada sahip bir yönteme sahip olmak anlamına gelir. Bu tür yöntemlerin tanımları ebeveyn ve alt sınıflarda farklıdır, ancak ad aynı kalır. Hatırlarsanız, Employee sınıfında bir give\_info() yöntemimiz vardı. Yönetici nesneleri hakkında takım boyutu bilgisi vermek için alt Yönetici sınıfında bu yöntemi geçersiz kılabiliriz.

```
class Manager(Employee):

    team_size = 10

    def set_team_size(self, team_size):
        self.team_size = team_size

    def give_info(self):
        print("Name:",self.name,"\nID:",self.employee_id,"\nTeam Size:",self.team_size)
        
muge = Manager("104", "Müge Özkan", 30)
muge.give_info()
```

Önceki örnekte gördüğünüz gibi, give\_info() yöntemi hem ebeveyn hem de alt sınıflar aracılığıyla çağrılmaktadır, ancak alt sınıf, üst sınıfın yöntemini geçersiz kıldığından farklı davranırlar.

## Multi Inheritance (Çoklu Miras)

Bir sınıfın ikiden fazla ebeveyn veya alt sınıfı olabilir.

```
```

## polymorphism

Polimorfizm, bir nesnenin farklı şekillerde hareket etme yeteneğini ifade eder. İki tür polimorfizm vardır: yöntem geçersiz kılma ve yöntem aşırı yükleme.

### Method overriding

Yöntem geçersiz kılma, alt sınıfta üst sınıfta olduğu gibi aynı ada sahip bir yönteme sahip olmak anlamına gelir. Bu tür yöntemlerin tanımları ebeveyn ve alt sınıflarda farklıdır, ancak ad aynı kalır. Hatırlarsanız, Employee sınıfında bir give\_info() yöntemimiz vardı. Yönetici nesneleri hakkında takım boyutu bilgisi vermek için alt Yönetici sınıfında bu yöntemi geçersiz kılabiliriz.

```
class Manager(Employee):

    team_size = 10

    def set_team_size(self, team_size):
        self.team_size = team_size

    def give_info(self):
        print("Name:",self.name,"\nID:",self.employee_id,"\nTeam Size:",self.team_size)
        
muge = Manager("104", "Müge Özkan", 30)
muge.give_info()
```

Önceki örnekte gördüğünüz gibi, give\_info() yöntemi hem ebeveyn hem de alt sınıflar aracılığıyla çağrılmaktadır, ancak alt sınıf, üst sınıfın yöntemini geçersiz kıldığından farklı davranırlar.

### Method overloading <a href="#method-overriding" id="method-overriding"></a>

Bu tür yöntemleri çağırırken argümanların sayısını veya türlerini değiştirerek herhangi bir yöntemi aşırı yükleyebilirsiniz ve yöntemler farklı davranır. Aşağıdaki örnekte, hesapla\_salary() yöntemini bir argümanla çağırırsak, o argümanı döndürür. Ancak, bu yöntemi iki argümanla çağırırsak, iki argümanın bir toplamını döndürür.

```
class Manager(Employee):

    team_size = 10

    def set_team_size(self, team_size):
        self.team_size = team_size

    def give_info(self):
        print("Name:",self.name,"\nID:",self.employee_id,"\nTeam Size:",self.team_size)

    def calculate_salary(self, salary, bonus=None):
        if bonus is not None:
            salary += bonus
        return salary
```

```python
muge = Manager("104", "Müge Özkan", 30)
muge.calculate_salary(12345) 
muge.calculate_salary(12345, 678)
```

## dunder (magic) methods
