## Python f-strings can do more than you thought

In this Article I'm going to be talking about ```f-strings``` and some of the cool things that you can do with them. so most of you are probably already aware of what f strings are.

# 🎯 f-strings 

<p>
Also called “formatted string literals,” f-strings are string literals that have an f at the beginning and curly braces containing expressions that will be replaced with their values.
</p>

## 1.Put a '='  Sign afterwards
One of the really cool things that you can do is just put an equals sign afterwards,eg-

### Code - 
```python
word = 'Hello World'
num = 152
print(f'The value of word is f{word}')
print(f'{word=}')

print(f'The value of num is f{num}')
print(f'{num=}')
print(f'{num + 8 =}')
```
### Output - 
```txt
The value of word is Hello World
word='Hello World'
The value of num is f152
num=152
num + 8 =160
```
 
## 2.Conversions

<p>
So if you're not aware,  inside the curly braces of an f string after the expression you can put a ```!a ,!s , !r ``` , and 
what these do is instead of printing the value of this thing, it will additionally do some extra thing on top of that.
</p>
<br>
<p>
!r - repr() 'The repr() method returns a string containing a printable representation of an object.'

!a - ascii 'all the non ascii characters get replaced with an ascii safe escaped version of it'
 
 !s - string conversion operator 'formating'
</p>


### Code - 
```python
def conversion():
    str_value = "Hello World 😀"
    print(f'{str_value!r}')
    print(f'{str_value!a}')
    print(f'{str_value!s}')

conversion()

```

### Output - 
```
'Hello World 😀'
'Hello World \U0001f600'
Hello World 😀
```



## 3.Formatting

<p>
':' after the variable 
</p>

### Code -

```python
import datetime

def formatting():
    num_value = 475.2486
    now = datetime.datetime.utcnow()

    #Formats the datee in the given format
    print(f'{now=:%Y-%m-%d}')

    # Rounds the decimal to 2 digits
    print(f'{num_value:.2f}')

formatting()
```

### Output -
```
now=2021-08-04
475.25
```