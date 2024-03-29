# Inheritance

Arkadaşlar merhaba,

Bir önceki dersimizde sınıfları anlatmıştık. Ne işe yarıyordu sınıflar ? Sınıflar nesnelerin özelliklerini ve davranışlarını tanımlayan yapılardı. Yani bize nesnenin nasıl olacağı ile ilgili bir şablon sunuyordu. Daha sonra biz o şablonu kullanarak nesnelerimizi oluşturuyorduk.

Neleri vardı sınıflarımızın atrributes (özellikleri) ve methodları (davranışları).

Bu dersimizde kalıtım (inheritance) göreceğiz. Kalıtım, bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını miras almasına izin veren bir nesne yönelimli programlama özelliğidir.

Hemen basit bir örnek ile başlayalım.&#x20;

Hayvanlar için sınıflar tanımlayalım. Öncelikle Kopek sınıfı ile başlayalım.



## kopek sınıfı

```python
class Kopek:
    mama = 200
    # constructor
    def __init__(self, isim, soyisim, yas):
        self.isim = isim
        self.soyisim = soyisim
        self.yas = yas

    def beslenme(self):
        print(f'{self.isim} {self.soyisim} gunde {self.mama} gr mama yiyor.')

    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} hareket ediyor')

kaptan = Kopek('Kaptan', 'Bir', 5)

print(kaptan.isim)
kaptan.beslenme()
kaptan.hareket_et()

```

```python
class Buldog(Kopek):
    mama = 300

    
rocky = Buldog('Rocky', 'Rock', 1)

print(rocky)
print(rocky.isim)
rocky.beslenme()
rocky.hareket_et()


class KurtKopegi(Kopek):
    mama = 400

asi = KurtKopegi('Asi', 'Bey', 3)
asi.beslenme()
```

Bir tane de kedi sınıfı oluşturalım.

## kedi sınıfı

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
        print(f'{self.isim} {self.soyisim} ses cikariyor')
        print('miyaw')
        
dantel= Kedi('Dantel', 'Ocean', 3)

print(dantel)
print(dantel.isim)
dantel.beslenme()
dantel.hareket_et()
dantel.ses_cikar()
```

Daha önceki konularda ne demiştik DRY prensinimiz vardı değil mi? Neydi DRY prensibi ? Dont Repeat Yourself.&#x20;

Adından da anlaşılacağı üzere gereksiz kod tekrarlarının önüne geçmeyi amaçlayan bir tasarım ilkesiydi. Kedi ve Kopek sınıfımıza baktığımızda bu ilkeye uymadığını açıkça görüyoruz.&#x20;

Kalıtım (inheritance) içinj ne demiştik, bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını miras almasına izin veren bir nesne yönelimli programlama özelliğidir.&#x20;

Kalıtım, kod tekrarını önlemek, kodu daha anlaşılır ve sürdürülebilir hale getirmek için kullanılır. O zaman biz base bir sınıf yapıp bu sınıflarımızı o sınıftan türetebiliriz.

## hayvan sınıfı

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

dantel= Kedi('Dantel', 'Ocean', 3)

print(dantel)
print(dantel.isim)
dantel.beslenme()
dantel.hareket_et()
```

## add new method

```python
class Kopek(Hayvan):
    def ses_cikar(self):
        print('hav hav')


class Kedi(Hayvan):
    def ses_cikar(self):
        print('miyav')
```

## override

```python
class Kus(Hayvan):
    def hareket_et(self):
        print(f'{self.isim} {self.soyisim} uçuyor')
        
    def ses_cikar(self):
        print('cik cik')
```

## init override

## super()

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

DRY yine uymadı

```python
class Kedi(Hayvan):

    def __init__(self, isim, soyisim, yas, cins):
        super().__init__(isim, soyisim, yas)
        self.cins = cins

    def ses_cikar(self):
        print('miyav')
```

```python
dantel = Kedi('Dantel', 'Ocean', 3, 'British')

print(dantel)
print(dantel.cins)
dantel.beslenme()
dantel.hareket_et()
```

## isinstance

```python
print(isinstance(dantel, Kedi))
print(isinstance(dantel, Kopek))
print(isinstance(dantel, Hayvan))
```

## issubclass

```python
print(issubclass(Kedi, Kopek))
print(issubclass(Kedi, Hayvan))
```

## private, protected, public











## kalıtım türleri

single&#x20;

```python
class Hayvan:
    def aciklama(self):
        print('Hayvan')
        

class Kedi(Hayvan):
    def aciklama(self):
        print('Kedi')
        
obj = Kedi()
obj.aciklama()

# Kedi

class Hayvan:
    def aciklama(self):
        print('Hayvan')
        

class Kedi(Hayvan):
    pass
        
obj = Kedi()
obj.aciklama()

# Hayvan
```

multilevel

```python
class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Memeli(Hayvan):
    def aciklama(self):
        print('Memeli')


class Kedi(Memeli):
    def aciklama(self):
        print('Kedi')
        

obj = Kedi()
obj.aciklama()

# Kedi


class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Memeli(Hayvan):
    def aciklama(self):
        print('Memeli')


class Kedi(Memeli):
    pass
    
# Memeli
```

multiple&#x20;

```python
class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Evcil:
    def aciklama(self):
        print('Evcil')


class Kedi(Hayvan, Evcil):
    def aciklama(self):
        print('Kedi')
     
obj = Kedi()
obj.aciklama()
   
# Kedi


class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Evcil:
    def aciklama(self):
        print('Evcil')


class Kedi(Evcil, Hayvan):
    pass
    
    
obj = Kedi()
obj.aciklama()

# Evcil


class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Evcil:
    pass


class Kedi(Evcil, Hayvan):
    pass
    
    
obj = Kedi()
obj.aciklama()

# Hayvan

```

hierarchical

```python
class Hayvan:
    def aciklama(self):
        print('Hayvan')


class Kedi(Hayvan):
    def aciklama(self):
        print('Kedi')


class Kopek(Hayvan):
    def aciklama(self):
        print('Köpek')
```

hybrid

```python
class Hayvan:
    def aciklama(self):
        print('Hayvan')
    
class At(Hayvan):
    def aciklama(self):
        print('At')
    
class Esek(Hayvan):
    def aciklama(self):
        print('Esek')
    
class Katir(At, Esek):
    def aciklama(self):
        print('Katir')

obj = Katir()
obj.aciklama()

# Katir


class Hayvan:
    def aciklama(self):
        print('Hayvan')
    
class At(Hayvan):
    pass
    
class Esek(Hayvan):
    def aciklama(self):
        print('Esek')
    
class Katir(At, Esek):
    pass

obj = Katir()
obj.aciklama()

# Esek
```

## mixins

## MRO - Method Resolution Order

```python
print(Katir.mro())
print(Katir.__mro__)
print(help(Katir))
```





## örnek

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

    def personel_ekle(self, p):
        if p not in self.personeller:
            self.personeller.append(p)
        else:
            print('Bu personel zaten ekli')

        self.personel_listele()

    def personel_sil(self, p):
        if p in self.personeller:
            self.personeller.remove(p)
        else:
            print('Bu personel ekli değil')

        self.personel_listele()

    def personel_listele(self):
        for p in self.personeller:
            print('-->', p.full_name)


class YazilimYonetici(Manager):
    maas_katsayisi = 2.5
    
    def personel_ekle(self, p):
        if isinstance(p, Yazilimci):
            if p not in self.personeller:
                self.personeller.append(p)
            else:
                print('Bu personel zaten ekli')
        else:
            print('Bu personel yazılımcı değil')
```

\


\
