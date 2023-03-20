# Pandas Import

```python
import pandas as pd

# Excel dosyasını import etme
# Sadece ilk sheet yüklenir

df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx')

# Excel dosyasındaki tüm sheetleri alma
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name=None)
df.keys() # df['DATA1']

# Excel dosyasındaki belirli sheetleri alma. 0 ve 1. sıradaki sheetler ve 'DATA2'sheet alınır
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name=[0, 1, 'DATA2'])
df.keys() # dict_keys([0, 1, 'DATA2'])

# Excel dosyasındaki belirlibelirli bir sheet içerisindeki verileri alma
# ikinci sıradaki sheet alınır
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name=1)

# DATA1 isimli sheet alınır
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1')

# baştaki bir satırı yok sayma
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1', skiprows=1)

# belirli sütunlar arasını alma
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1', skiprows=1, usecols='B:E')

# sütun isimlerini yok ise
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1', skiprows=1, usecols='B:E', header=None)

# istediğimiz sütun isimleri ekleyebiliriz eğer sütun isimleri yok ise yine header=None unutulmamalı
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1', skiprows=1, usecols='B:E', names=['A','B','C','D'])

# eğer sütunlar arasında index var ise seçme için index_col sırasını göndeririz.
df = pd.read_excel('kalibrasyon/Data_KURTIC_20221231.xlsx', sheet_name='DATA1', skiprows=1, usecols='B:E', index_col=0)

# skipfooter : sondan alınmayacak satır sayısı
# thousands : binlik ayıracı
# decimal : ondalık ayıracı
# dtype : alınan alanların türleri
# nrows : kaç satır alınacağı
# parse_dates : tarihler otomatik olarak çevrilsin
# eğer data sadece tek bir sütundan oluşuyorsa Series dönmesi için squueze True seçilir

df
```

```python
df = pd.read_csv('kalibrasyon/2020-2021.csv')

# sep = ','
# ayıraç seçmek için
df = pd.read_csv('kalibrasyon/2020-2021.csv', sep=';')

# eğer ilk satır başlık değilse header=None
df = pd.read_csv('kalibrasyon/2020-2021.csv', sep=';', header=None)

# sütun isimleri names ile belirlenebilir
df = pd.read_csv('kalibrasyon/2020-2021.csv', sep=';', names=[1,3,4,7])
```

```python
# tek sheet yazdırmak için
df.to_excel('kalibrasyon/aaa.xlsx')

# birden fazla sheet yazdırmak için
df2 = df.copy()
with pd.ExcelWriter('kalibrasyon/bbb.xlsx') as writer:
    df.to_excel(writer, sheet_name='Sheet_name_1', freeze_panes=(1,1))
    df2.to_excel(writer, sheet_name='Sheet_name_2')

df2.to_excel('kalibrasyon/ccc.xlsx', engine='xlsxwriter')

with pd.ExcelWriter('kalibrasyon/bbb.xlsx', engine="openpyxl", mode='a') as writer:
    df.to_excel(writer, sheet_name='Sheet_name_3')

# startrow
# startcol
# columns : Columns to write.
# header
```
