# Inheritance

Arkadaşlar merhaba,

Bir önceki dersimizde sınıfları anlatmıştık. Ne işe yarıyordu sınıflar ? Sınıflar nesnelerin özelliklerini ve davranışlarını tanımlayan yapılardı. Yani bize nesnenin nasıl olacağı ile ilgili bir reçete / şablon sunuyordu.

Neleri vardı sınıflarımızın atrributes (özellikleri) ve methodları (davranışları).

Bu dersimizde kalıtım (inheritance) göreceğiz. Kalıtım, bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını miras almasına izin veren bir nesne yönelimli programlama özelliğidir.

Hemen basit bir örnek ile başlayalım.&#x20;

Hayvanlar için sınıflar tanımlayalım. Öncelikle Kopek sınıfı ile başlayalım.

```python
class Kopek:
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

```
// Some code
```









\
