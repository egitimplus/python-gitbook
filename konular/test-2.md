# Test

{% hint style="info" %}
LESSER OF TWO EVENS

Write a function that returns the lesser of two given numbers if both numbers are even, but returns the greater if one or both numbers are odd

lesser\_of\_two\_evens(2,4) --> 2&#x20;

lesser\_of\_two\_evens(2,5) --> 5
{% endhint %}

<pre class="language-python"><code class="lang-python">def lesser_of_two_evens(a,b):
    if a%2 == 0 and b%2 == 0:
        return min(a,b)
    else:
        return max(a,b)
        
# Check
<strong>print(lesser_of_two_evens(2,4))     # 2
</strong>print(lesser_of_two_evens(2,4))THO  # 5</code></pre>

{% hint style="info" %}
ANIMAL CRACKERS

Write a function takes a two-word string and returns True if both words begin with same letter

animal\_crackers('Levelheaded Llama') --> True&#x20;

animal\_crackers('Crazy Kangaroo') --> False
{% endhint %}

```python
def animal_crackers(text):
    wordlist = text.split()
    return wordlist[0][0] == wordlist[1][0]
    
# Check
animal_crackers('Levelheaded Llama')  # True
animal_crackers('Crazy Kangaroo')     # False
```

{% hint style="info" %}
MAKES TWENTY

Given two integers, return True if the sum of the integers is 20 or if one of the integers is 20. If not, return False

makes\_twenty(20,10) --> True&#x20;

makes\_twenty(12,8) --> True&#x20;

makes\_twenty(2,3) --> False
{% endhint %}

```python
def makes_twenty(n1,n2):
    return (n1+n2)==20 or n1==20 or n2==20
    
# Check
makes_twenty(20,10) # True
makes_twenty(12,8)  # True
makes_twenty(2,3)   # False
```

{% hint style="info" %}
OLD MACDONALD

Write a function that capitalizes the first and fourth letters of a name

old\_macdonald('macdonald') --> MacDonald
{% endhint %}

```python
def old_macdonald(name):
    if len(name) > 3:
        return name[:3].capitalize() + name[3:].capitalize()
    else:
        return 'Name is too short!'
        
# Check
print(old_macdonald('macdonald')) 
# MacDonald
```

{% hint style="info" %}
MASTER YODA

Given a sentence, return a sentence with the words reversed

master\_yoda('I am home') --> 'home am I'&#x20;

master\_yoda('We are ready') --> 'ready are We'
{% endhint %}

<pre class="language-python"><code class="lang-python">def master_yoda(text):
    return ' '.join(text.split()[::-1])
    
# Check
<strong>print(master_yoda('I am home'))    # home am I
</strong>print(master_yoda('We are ready')) # ready are We
</code></pre>

{% hint style="info" %}
ALMOST THERE

Given an integer n, return True if n is within 10 of either 100 or 200

almost\_there(90) --> True&#x20;

almost\_there(104) --> True&#x20;

almost\_there(150) --> False&#x20;

almost\_there(209) --> True
{% endhint %}

```python
def almost_there(n):
    return ((abs(100 - n) <= 10) or (abs(200 - n) <= 10))
    
# Check
print(almost_there(90))  # True
print(almost_there(104)) # True
print(almost_there(150)) # False
print(almost_there(209)) # True
```

{% hint style="info" %}
FIND 33

Given a list of ints, return True if the array contains a 3 next to a 3 somewhere.&#x20;

has\_33(\[1, 3, 3]) → True&#x20;

has\_33(\[1, 3, 1, 3]) → False&#x20;

has\_33(\[3, 1, 3]) → False
{% endhint %}

<pre class="language-python"><code class="lang-python">def has_33(nums):
    for i in range(0, len(nums)-1):
      
        # nicer looking alternative in commented code
        #if nums[i] == 3 and nums[i+1] == 3:
    
        if nums[i:i+2] == [3,3]:
            return True  
    
    return False
    
# Check
print(has_33([1, 3, 3]))    # True
<strong>print(has_33([1, 3, 1, 3])) # False
</strong>print(has_33([3, 1, 3]))    # Falsey</code></pre>

{% hint style="info" %}
PAPER DOLL

Given a string, return a string where for every character in the original there are three characters&#x20;

paper\_doll('Hello') --> 'HHHeeellllllooo'&#x20;

paper\_doll('Mississippi') --> 'MMMiiissssssiiippppppiii'
{% endhint %}

```python
def paper_doll(text):
    result = ''
    for char in text:
        result += char * 3
    return result
    
# Check
print(paper_doll('Hello'))         #'HHHeeellllllooo'
print(paper_doll('Mississippi'))   # 'MMMiiissssssiiissssssiiippppppiii'
```

{% hint style="info" %}
BLACKJACK: Given three integers between 1 and 11, if their sum is less than or equal to 21, return their sum. If their sum exceeds 21 and there's an eleven, reduce the total sum by 10. Finally, if the sum (even after adjustment) exceeds 21, return 'BUST'&#x20;

blackjack(5,6,7) --> 18&#x20;

blackjack(9,9,9) --> 'BUST'&#x20;

blackjack(9,9,11) --> 19
{% endhint %}

```python
def blackjack(a,b,c):
    if sum((a,b,c)) <= 21:
        return sum((a,b,c))
    elif sum((a,b,c)) <=31 and 11 in (a,b,c):
        return sum((a,b,c)) - 10
    else:
        return 'BUST'
        
# Check
blackjack(5,6,7)  # 18
blackjack(9,9,9)  # 'BUST'
blackjack(9,9,11) # 19
```

{% hint style="info" %}
SUMMER OF '69: Return the sum of the numbers in the array, except ignore sections of numbers starting with a 6 and extending to the next 9 (every 6 will be followed by at least one 9). Return 0 for no numbers.&#x20;

summer\_69(\[1, 3, 5]) --> 9&#x20;

summer\_69(\[4, 5, 6, 7, 8, 9]) --> 9&#x20;

summer\_69(\[2, 1, 6, 9, 11]) --> 14
{% endhint %}

```python
def summer_69(arr):
    total = 0
    add = True
    for num in arr:
        while add:
            if num != 6:
                total += num
                break
            else:
                add = False
        while not add:
            if num != 9:
                break
            else:
                add = True
                break
    return total
    
# Check
summer_69([1, 3, 5])          # 9
summer_69([4, 5, 6, 7, 8, 9]) # 9
summer_69([2, 1, 6, 9, 11])   # 14
```

{% hint style="info" %}
SPY GAME

Write a function that takes in a list of integers and returns True if it contains 007 in order&#x20;

spy\_game(\[1,2,4,0,0,7,5]) --> True&#x20;

spy\_game(\[1,0,2,4,0,5,7]) --> True&#x20;

spy\_game(\[1,7,2,0,4,5,0]) --> False
{% endhint %}

```python
def spy_game(nums):

    code = [0,0,7,'x']
    
    for num in nums:
        if num == code[0]:
            code.pop(0)   # code.remove(num) also works
       
    return len(code) == 1
    
# Check
print(spy_game([1,2,4,0,0,7,5])) # True
print(spy_game([1,0,2,4,0,5,7])) # True
print(spy_game([1,7,2,0,4,5,0])) # False
```

{% hint style="info" %}
COUNT PRIMES

Write a function that returns the number of prime numbers that exist up to and including a given number&#x20;

count\_primes(100) --> 25&#x20;

By convention, 0 and 1 are not prime.
{% endhint %}

```python
def count_primes(num):
    primes = [2]
    x = 3
    if num < 2:  # for the case of num = 0 or 1
        return 0
    while x <= num:
        for y in range(3,x,2):  # test all odd factors up to x-1
            if x%y == 0:
                x += 2
                break
        else:
            primes.append(x)
            x += 2
    print(primes)
    return len(primes)
    
# Check
print(count_primes(100))

# [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97]
# yt25
```

```python
# BONUS: Here's a faster version that makes use of the prime numbers we're collecting as we go!

def count_primes2(num):
    primes = [2]
    x = 3
    if num < 2:
        return 0
    while x <= num:
        for y in primes:  # use the primes list!
            if x%y == 0:
                x += 2
                break
        else:
            primes.append(x)
            x += 2
    print(primes)
    return len(primes)o
```
