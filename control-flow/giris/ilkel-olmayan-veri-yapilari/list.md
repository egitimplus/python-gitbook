# List

* Sıralanabilir (ordered), Değiştirilebilir (mutable), Tekrarlanabilir (duplicate)

<pre><code><strong># Boş Liste Tanımlama
</strong>my_list = list()
my_list = []
print(my_list) 
# Output: []

# Elemanı olan liste oluşturma
my_list = ['Newyork', 'London', 'Paris']
my_list = list(('Newyork', 'London', 'Paris'))

print(my_list) 
# Output: ['Newyork', 'London', 'Paris']

# Listelere farklı türlerde eleman eklenebilir
my_list = ['Newyork', 3, 3.5, True, ['banana', 'orange']]
print(my_list) 
# Output: ['Newyork', 3, 3.5, True, ['banana', 'orange']]

# Listenin eleman sayısı için len() metodunu kullanırız
print(len(my_list)) 
# Output: 3

# Listenin elemanlarına indexi ile ulaşılabilir. 
# Index aynı stringlerde olduğu gibi sıfırdan başlar.
print(my_list[2])
print(my_list[-1])</code></pre>
