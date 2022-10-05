# Auth

Check email

```
data = [
    'adam.com',
    'adam@.adam.com',
    'adam@adam.com.',
    'adam@adam.com'
    ]

print(check_emails(data))
# Output: ['adam@adam.com']
```

Kullanıcıya şifresine soralım. Şifresinde;

* 1 küçük harf
* 1 büyük harf
* 1 sayı olmalı
* boşluk olmamalı
* en az 8 karakter olmalı

Koşullara uygun şifre girilirse Başarıyla oluşturuldu diyelim. Değilse hatayı yazdıralım ve tekrar soralım.

```python

while True:
    password = input('Please enter your password: ')

    if len(password) < 8:
        print('Your password too short')
    else:
        decimal = lower = upper = False
        for char in password:
            if char.isspace():
                print('You cant use whitespace')
                break
            
            if char.isdecimal():
                decimal = True
            
            if char.islower():
                lower = True

            if char.isupper():
                upper = True

        if decimal and upper and lower:
            print('Your password is accepted')
            break
        else:
            print('You must use one lower, one upper and one digit.')

'''
Output:

Please enter your password: Emre Çevik
You cant use whitespace
You must use one lower, one upper and one digit.
Please enter your password: 1234!Python
Your password is accepted
'''
```

Bir kullanıcı formu olduğunu düşünelim kullanıcı şifresini girdiğinde (12345) ona şifrenizi girdiniz 5 karakter ('\*\*\*\*\*') uzunluğunda diye ekrana yazdıralım

```python
def password_count():
    password = input('Please enter password: ')
    password_count = len(password)

    return password_count

pass_count = password_count()
print(f'Your password is {pass_count} ({pass_count * "*"}) characters long.')

'''
Output:

Please enter password: 123456
Your password is 6 (******) characters long.
'''
```

Kullanıcının kayıt formuna yazdığı email adresinden kullanıcı adı oluşturan bir fonksiyon yazacağız. @ işaretinden önceki kısmı kullanıcı adı olacak.

```python
def create_user_from_email(email):

    if email.count(' ') > 0:
        return 'You dont use whitespaces'

    if email.count('@') > 1:
        return 'You must only one @'
    
    if email.count('@') == 0:
        return 'You must use one @'

    if email[-1] == '@' or email[0] == '@':
        return 'You must use @ in the middle'

    split_email = email.split('@')

    if split_email[1].count('.') == 0:
        return 'You must use . for domain'

    if split_email[1][-1] == '.' or split_email[1][0] == '.':
        return 'You must use . in the middle'

    return split_email[0]

print(create_user_from_email('emrecevik@sas.ss'))
# Output: emrecevik
```

Username Generator

Kullanıcının kayıt formuna yazadığı isim ve soyisimden kullanıcı adı oluşturan bir fonksiyon yazacağız.

Eğer o kullanıcı adı varsa sonuna 1 ekleyeceğiz. Eğer sonunda kullandığımız sayıda varsa 2, 3 diye olmayana kadar ilerleyeceğiz.

Boş karakterler silinecektir.

```python
user_data = [
    'adamsmith',
    'johnwick'
]

def user_info(data):
    name = input('Please enter name: ')
    surname = input('Please enter surname: ')

    username = name.replace(' ', '').lower() + surname.replace(' ', '').lower()
    
    i = 0
    while True:        
        username = username if i == 0 else username + str(i)
        
        if username not in data:    
            data.append(username)
            return username
        i = i + 1

    return username

print(user_info(user_data))

'''
Output:

Please enter name: Adam
Please enter surname: Smith
adamsmith1

'''

```

