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

## encapsulation

Nesne yönelimli programlamada üç ana kavram vardır: Kapsülleme, Kalıtım ve Polimorfizm. Kapsülleme, veri gizleme anlamına gelir. OOP'de, bir sınıfın diğer sınıfın verilerine doğrudan erişimi olmamalı veya erişim, örnek yöntemlerle kontrol edilmelidir. Sınıf verilerine erişimi kontrol etmek için özel değişkenleri ve özellikleri kullanabilirsiniz. Özel bir değişken tanımlamak için değişken adının önüne iki alt çizgi koyabilirsiniz. Örneğin, \_\_age özel bir değişkendir. Aşağıdaki kodda gösterildiği gibi bu mantığı uygulayan age özniteliği için bir özellik oluşturabilirsiniz. Bir mülkün üç bölümü vardır. Aşağıdaki örnekte age olan özniteliği tanımlamanız gerekir. Ardından, @property dekoratörünü kullanarak özniteliğin özelliğini tanımlamanız gerekir. Son olarak, aşağıdaki örnekte @age.setter tanımlayıcısı olan bir özellik ayarlayıcı oluşturmalısınız. Çalışanların yaşının her zaman 18 - 99 arasında olması gerektiğini söyleyebilirsiniz. Bir kullanıcı yaş özniteliği için 18'den küçük veya 99'dan büyük bir değer girmeye çalışırsa, bir hata vardır ve Employee sınıfından bir nesne oluşturulamaz. . Ancak değer 18 - 99 arasındaysa bir nesne oluşturulabilir.

```
class Employee:

    #class attributes
    status = "active"
    number_of_employee = 0

    def __init__(self, employee_id, name, age):
        self.employee_id = employee_id #instance attribute
        self.name = name #instance attribute
        self.age = age #instance attribute
        Employee.number_of_employee += 1


    # Creates model property
    @property
    def age(self):
        return self.__age

    # Create property setter
    @age.setter
    def age(self, age):
        if age < 18:
            raise Exception('An Employee\'s age cannot be lower than 18')
        elif age > 99:
            raise Exception('An Employee\'s age cannot be upper than 99')
        else:
            self.__age = age


    #instance method
    def give_info(self):
        print("Name:",self.name,"\nID:",self.employee_id)

    @staticmethod
    def get_class_objective():
        message = "The objective of this Employee class is to organize employee information with more modular manner"
        print (message)
        
child = Employee("103", "Eric Cartman", 12)
# Exception: An Employee's age cannot be lower than 18

```

## inheritance

OOP'deki kalıtım, bir çocuğun kendi benzersiz özelliklerine ek olarak ebeveynlerinden bazı özellikleri miras aldığı gerçek dünya mirasına benzer. Başka bir sınıfı miras alan sınıfa alt sınıf, başka bir sınıf tarafından miras alınan sınıfa ise üst sınıf denir. Aşağıdaki kod, bir kalıtım örneği gösterir.

```
# Create Class Manager that inherits Employee
class Manager(Employee):

    def set_team_size(self, team_size):
        self.team_size = team_size
```

Önceki örnekte, Employee sınıfını miras alan bir Manager sınıfı oluşturuyorum. Bir sınıfı miras almak için, alt sınıf adından sonra gelen parantez içine üst sınıf adını yazmalısınız. Manager sınıfı, aşağıdaki örnekte gösterildiği gibi, ana Employee sınıfının tüm özniteliklerine ve yöntemlerine erişebilir.

```
muge = Manager("104", "Müge Özkan", 30)

muge.name
muge.status
muge.get_class_objective()
```

Manager sınıfının, Employee sınıfının yöntem ve niteliklerine ek olarak kendi set\_team\_size() yöntemi de vardır. Manager sınıfının nesnesinin takım boyutunu aşağıdaki örnekte olduğu gibi ayarlayabilirsiniz. Bir yan not olarak, bir sınıfın ikiden fazla ebeveyn veya alt sınıfı olabilir.

```
muge.set_team_size(10)
muge.team_size
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
