# Pandas Import

```python
import pandas as pd

# -------------------------------------------------------------------------
# Excel dosyasını import etme
# -------------------------------------------------------------------------
## Sadece ilk sheet yüklenir
df = pd.read_excel('data/diller.xlsx')

# -------------------------------------------------------------------------
# Excel dosyasındaki belirlibelirli bir sheet içerisindeki verileri alma
# -------------------------------------------------------------------------
## ikinci sıradaki sheet alınır
df = pd.read_excel('data/diller.xlsx', sheet_name=1)

## frontend alınır
df = pd.read_excel('data/diller.xlsx', sheet_name='frontend')

# -------------------------------------------------------------------------
# Excel dosyasındaki tüm sheetleri alma
# -------------------------------------------------------------------------
df = pd.read_excel('data/diller.xlsx', sheet_name=None)

## keyleri yazdırma
df.keys()

## backend datası yazdırma
df['backend']

# -------------------------------------------------------------------------
# Excel dosyasındaki belirli sheetleri alma. 
# -------------------------------------------------------------------------
# backend ve frontend alınır
df = pd.read_excel('data/diller.xlsx', sheet_name=['backend', 'frontend'])
df['backend']

# backend ve 2. sıradaki sheet alınır
df = pd.read_excel('data/diller.xlsx', sheet_name=['backend', 1])
df['backend']

# 1. ve 2. sıradaki sheet alınır
df = pd.read_excel('data/diller.xlsx', sheet_name=[0, 1])
df[1]
```



```python
# -------------------------------------------------------------------------
# Satır ve sütunları yok sayma
# -------------------------------------------------------------------------
df = pd.read_excel('data/sehirler.xlsx')

# baştaki üç satırı yok sayma
df = pd.read_excel('data/sehirler.xlsx', skiprows=3)

# sondaki iki satırı yok sayma
df = pd.read_excel('data/sehirler.xlsx', skipfooter=2)

# B:C arası sütunları alma
df = pd.read_excel('data/sehirler.xlsx', skiprows=3, usecols='B:C')

# alınacak satır sayısını bir olarak belirleme
df = pd.read_excel('data/sehirler.xlsx', skiprows=3, nrows=1)

```



<pre class="language-python"><code class="lang-python"><strong># -------------------------------------------------------------------------
</strong># Başlıklar ve Indeks
# -------------------------------------------------------------------------
# başlıksız olarak verileri alma
df = pd.read_excel('data/sehirler.xlsx', skiprows=3, usecols='B:C', header=None)

# başlık ekleme
df = pd.read_excel('data/sehirler.xlsx', skiprows=3, usecols='B:C', names=['City', 'Count'])

# eğer sütunlar arasında index var ise seçme için index_col sırasını göndeririz.
df = pd.read_excel('data/sehirler.xlsx', skiprows=3, usecols='B:C', index_col=0)

# thousands : binlik ayıracı
# decimal : ondalık ayıracı
# dtype : alınan alanların türleri
# parse_dates : tarihler otomatik olarak çevrilsin
</code></pre>



```python




```

1

```python
```

1

```python
```

1

```python
```

1

```python
// Some codeö0o
```

```python
import pandas as pd



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

[https://sparkbyexamples.com/pandas/pandas-create-dataframe-with-examples/](https://sparkbyexamples.com/pandas/pandas-create-dataframe-with-examples/)
