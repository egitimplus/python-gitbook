# Inheritance

Arkadaşlar merhaba,

Bir önceki dersimizde sınıfları anlatmıştık. Ne işe yarıyordu sınıflar ? Sınıflar nesnelerin özelliklerini ve davranışlarını tanımlayan yapılardı. Yani bize nesnenin nasıl olacağı ile ilgili bir reçete / şablon sunuyordu.

Neleri vardı sınıflarımızın atrributes (özellikleri) ve methodları (davranışları).

Bu dersimizde kalıtım (inheritance) göreceğiz. Kalıtım, bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını miras almasına izin veren bir nesne yönelimli programlama özelliğidir.

Hemen basit bir örnek ile başlayalım.&#x20;

Hayvanlar için sınıflar tanımlayalım. Öncelikle Kopek sınıfı ile başlayalım.

```python
class Kopek:

    # constructor
    def __init__(self, isim, soyisim, yas):
        self.isim = isim
        self.soyisim = soyisim
        self.yas = yas

    def beslenme(self):
        print(f'{self.isim} {self.soyisim} besleniyor')

    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} hareket ediyor')

    def ses_cikar(self):
        print('hav hav')

kopek1 = Kopek('Kaptan', 'Bir', 5)

print(kopek1.isim)
kopek1.beslenme()
kopek1.hareket_et()
kopek1.ses_cikar()
```

Bir tane de kedi sınıfı oluşturalım.

```python
class Kedi:
    def __init__(self, isim, soyisim, yas):
        self.isim = isim
        self.soyisim = soyisim
        self.yas = yas

    def beslenme(self):
        print(f'{self.isim} {self.soyisim} besleniyor')

    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} hareket ediyor')

    def ses_cikar(self):
        print('miyaw')
        
kedi1 = Kedi('Dantel', 'Ocean', 3)

print(kedi1)
print(kedi1.isim)
kedi1.beslenme()
kedi1.hareket_et()
kedi1.ses_cikar()
```

Daha önceki konularda ne demiştik DRY prensinimiz vardı değil mi? Neydi DRY prensibi ? Dont Repeat Yourself.&#x20;

Adından da anlaşılacağı üzere gereksiz kod tekrarlarının önüne geçmeyi amaçlayan bir tasarım ilkesiydi. Kedi ve Kopek sınıfımıza baktığımızda bu ilkeye uymadığını açıkça görüyoruz.&#x20;

Kalıtım (inheritance) içinj ne demiştik, bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını miras almasına izin veren bir nesne yönelimli programlama özelliğidir.&#x20;

Kalıtım, kod tekrarını önlemek, kodu daha anlaşılır ve sürdürülebilir hale getirmek için kullanılır. O zaman biz base bir sınıf yapıp bu sınıflarımızı o sınıftan türetebiliriz.

```python
class Hayvan:
    def __init__(self, isim, soyisim, yas):
        self.isim = isim
        self.soyisim = soyisim
        self.yas = yas

    def beslenme(self):
        print(f'{self.isim} {self.soyisim} besleniyor')

    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} hareket ediyor')


class Kopek(Hayvan):
    pass


class Kedi(Hayvan):
    pass
    
```

```python
kopek1 = Kopek('Kaptan', 'Bir', 5)

print(kopek1)
print(kopek1.isim)
kopek1.beslenme()
kopek1.hareket_et()

kedi1 = Kedi('Dantel', 'Ocean', 3)

print(kedi1)
print(kedi1.isim)
kedi1.beslenme()
kedi1.hareket_et()
```

add new method

```python
class Kopek(Hayvan):
    def ses_cikar(self):
        print('hav hav')


class Kedi(Hayvan):
    def ses_cikar(self):
        print('miyav')
```

override

```python
class Kus(Hayvan):
    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} uçuyor')
        
    def ses_cikar(self):
        print('cik cik')
```

super()

```python
class Kedi(Hayvan):

    def __init__(self, isim, soyisim, yas, cins):
        self.isim = isim
        self.soyisim = soyisim
        self.yas = yas
        self.cins = cins

    def ses_cikar(self):
        print('miyav')
```

```python
class Kedi(Hayvan):

    def __init__(self, isim, soyisim, yas, cins):
        super().__init__(isim, soyisim, yas)
        self.cins = cins

    def ses_cikar(self):
        print('miyav')
```

```python
kedi1 = Kedi('Dantel', 'Ocean', 3, 'British')

print(kedi1)
print(kedi1.cins)
kedi1.beslenme()
kedi1.hareket_et()
```

isinstance

```python
print(isinstance(kedi1, Kedi))
print(isinstance(kedi1, Kopek))
print(isinstance(kedi1, Hayvan))
```

issubclass

```python
print(issubclass(Kedi, Kopek))
print(issubclass(Kedi, Hayvan))
```

private, protected, public













* Single&#x20;

![](<.gitbook/assets/image (3).png>)

```python
class Hayvan:
    pass
        

class Kedi(Hayvan):
    pass
```

* Multilevel

![](<.gitbook/assets/image (10).png>)

```python
class Hayvan:
    pass


class Memeli(Hayvan):
    pass


class Kedi(Memeli):
    pass
```

* Multiple&#x20;

![](<.gitbook/assets/image (2).png>)

```python
class Hayvan:
    pass


class Evcil:
    pass


class Kedi(Hayvan, Evcil):
    pass
```

* Hierarchical

![](<.gitbook/assets/image (1).png>)

```python
class Hayvan:
    pass


class Kedi(Hayvan):
    pass


class Kopek(Hayvan):
    pass
```

* Hybrid

![](<.gitbook/assets/image (11).png>)

```python
class University:
    pass
    
class Course(University):
    pass
    
class Branch(University):
    pass
    
class Student(Course, Branch):
    pass
    
```

MRO - Method Resolution Order

```python
print(Student.mro())
print(Student.__mro__)
print(help(Student))
```

Mixins





Örnek

```python
class Personel:
    maas_katsayisi = 1

    def __init__(self, isim, soyisim, maas):
        self.isim = isim
        self.soyisim = soyisim
        self.maas = maas

    def ad(self):
        return f'{self.isim} {self.soyisim}'

    def maas_hesapla(self):
        return self.maas * self.maas_katsayisi


class Muhasebe(Personel):
    pass


emre = Muhasebe('Emre', 'Çevik', 10000)
print(emre.ad())
print(emre.maas_hesapla())


class Yazilimci(Personel):
    maas_katsayisi = 1.5

    def __init__(self, isim, soyisim, maas, dil):
        super().__init__(isim, soyisim, maas)
        self.dil = dil

ali = Yazilimci('Ali', 'Can', 10000, 'python')

print(ali.ad())
print(ali.maas_hesapla())
print(ali.dil)


class Yonetici(Personel):
    maas_katsayisi = 2.1

    def __init__(self, isim, soyisim, maas, personeller=None):
        super().__init__(isim, soyisim, maas)

        if personeller is None:
            self.personeller = []
        else:
            self.personeller = personeller

    def personel_ekle(self):
        pass

    def personel_sil(self):
        pass

    def personel_listele(self):
        pass

```

Polymorphism

Abstract Base Class

\


\
