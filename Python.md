# Python

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
http://automatetheboringstuff.com/chapter1/
```

## Django


```console
andrew@DESKTOP:~$ python3 -m venv test_env      # Creates a new virtual environment called test_env
andrew@DESKTOP:~$ source test_env/bin/activate  # Activate the virtual environment
andrew@DESKTOP:~$ deactivate                    # (test_env) Deactivate the virtual environment
andrew@DESKTOP:~$ pip install django            # (test_env) Install django

andrew@DESKTOP:~$ django-admin startproject learning_log .  
<!-- Creates a new Django project in current directory -->  
# Creates a folder learning_log with python source files,
# and also a manage.py file in the top level which can be run with commands

andrew@DESKTOP:~$ python manage.py migrate  
# This manage.py migrate command tells django to make sure the database matches the current state of the project
# If no database exists (as in first run), it will create the database - a single file db.sqlite3



```


## Classes
```python
# A class is a blueprint of an object. 
# An object contains methods (ie specific functions) and attributes (ie specific variables)
# A class always starts with an __init__ method - that initialises it (ie a constructor method)
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
    
  def say_hello(self):
    print(f"Hello, my name is {self.name}")
```



## Functions
```python
def hello(first_name, last_name):
  print(first_name + " " + last_name)
 
# You can use a keyword argument to explcicitly state what your arguments are when calling a function
# this can override the default order of arguments
def book(author, title):
  print(f"{title}, written by {author}")
  
book(title = 'Catch 22', author = 'Joseph Heller')

# You can provide default values for arguments that will be used if none are specified when the function is called
def person(name, sex = 'male'):
    print(f"{name} is {sex}.")

person('Andrew')

# You can define a function that will work with any given amount of arguments through *varibales
# The function will receive the arguments as a tuple (ie an immutable list)
# Often this is called *args
def function_name (*args):
  for each in args:
    print(each)
# This can be mixed with other arguments, but the variable number arg must come last
def add_numbers(num_1, num_2, all_remaining_numbers*):
  
# You can define a function that will accept a variable amount of keyword values using **
# When the last argument is defined as **arg, the function will create a dictionary and 
# save all keyword values into that dictionary
# Often this variable is called **kwargs
def build_profile(first, last, **user_info):
  user_info['first_name'] = first     # Adding the first argument as a value to the dictionary the function created
  user_info['last_name'] = last
  return user_info
  
# When adding keyvalues args, don't use quotes on the key, and don't use spaces between the =
temp = build_profile("andrew", "lim", height=178, city="Newcastle") 

```

## Flow

*Boolean*
```python
while True:   # Note capitalisation
```

*Operators*
```python
2 ** 3    # exponent            2 ** 3 = 8
22 // 8   # floored quotient   22 // 8 = 2
22 % 8    # modulus             22 % 8 = 6
```
*Falsy Values*
```python
name = ''
while not name:                        # String name is evaluated to be true if it is not empty
    print('Enter your name:')
    name = input()
print('How many guests will you have?')
numOfGuests = int(input())
if numOfGuests:                       # int numOfGuests is evalutated to be true of not 0
    print('Be sure to have enough room for all your guests.')
print('Done')
```


## Structure

*Defining a Function*

## Data

*Dictionaries*  

```python
# Dictionaries are Python's implementation of a data structure generally known as an asasociative array.
# A dictionary consists of a collection of key-value pairs. Each key-value pair maps the key to its associated value.
# It is similar to a list in that it is mutable, dynamic and can be nested.
# It differs in that elements are accessed through a key and not an index. Although access does not depend on order,
# due to the Python implementation the order does remain consistent, and as of Python 3.7
# this is guaranteed by language specification. https://realpython.com/python-dicts/
```

```python
capital_cities = {'australia' : 'sydney', 'united kingdom' : 'london'}     # defining a dictionary
print(f"The capital city of Australia is {capital_cities['australia']}")   # accessing the value for a key
capital_cities['australia'] = 'sydney'               # modifying a value
capital_cities['united states'] = 'washington d.c'   # adding a new value
del capital_cities['australia']                      # removing a value using del statement
capital_cities.get('canada', ('key not found') # get() method can be used without causing crash if key doesn't exist

# Looping with access to key and value
for country, city in capital_cities.items():   # for key, value, in dict.items():
  print(f"{country} -- {city}

# Looping with access to just values
for city in capital_cities.values():    # .values() is optional as this is the default behaviour for loop on dictionary
  print(f"--{city}")
  
# Looping with access to just keys
for country in capital_cities.keys():
  print(f"--{country}")
  
# Checking for existance of key without loop
if 'canada' not in capital_cities.keys():         # capital_cities.keys() returns a list of keys from the dictionary
    print('Canda is not in dicitonary')
  
```

*Strings*
```python
name = "ada lovelace"
print(name.title())  # Altering Case examples
print(name.upper())
print(name.lower())
greetingMsg = f"Hello, {name}! Thanks for joining"  # Using String format
print("Languages:\n\tPython\n\tC++\n\tJavascript")  # Newline and tab
name = "  andrew "
name.strip()  # remove leading and ending whitespace
              # also has left/right lstrip() rstrip() versions
```

*Lists*
```python
names = ['andrew', 'lisa', 'julie-ann']       # initialise a list
squares = [value**2 for value in range(6)]    # list generated from a sequence in 1 line, called list comprehension
print(names[1])                               # accessing an element
names.append('garry')                         # adding an element
names.insert(2, 'margaret')                   # inserting an element
del names[0]                                  # removing an element with del statement and index
removed_person = names.pop()                  # pop() method references element and then removes
removed_person = names.pop(2)                 # can be used on index
names.remove('lisa')                          # remove() removes (first) matching element
names.sort()                                  # sort by alphabet - can take parameter reverse=True
sorted(names)                                 # function that makes a new copy of list that is sorted
len(names)                                    # function that displays amount of elements in list (length)
numbers[3:6]                                  # returns a new list 'slice', starting (inclusive) and ending (exclusive)
numbers[:3]                                   # returns first 3 elements
numbers[-3:]                                  # returns last 3 elements
numbers_copy = numbers[:]                     # using slice to create a new list that is a copy of an original
min(numbers)                                  # returns smallest number
max(numbers)                                  # returns largest number
sum(numbers)                                  # returns total of all numbers in the list
numbers = list(range1, 6)                     # using list() function to convert a range data type straight to a list
if numbers:                                   # referencing the list serves as boolean expression whether it is empty
  print("numbers has elements")
else:
  print("numbers is an empty list")
```

*Tuples*
```python
foods = ('meat', 'potato', 'eggs')            # a tuple is an immutable list, created using round brackets 
```

*Casting*
```python
str(45)     # casting int to String 
int(1.25)   # casting float to int
float(10)   # casting int to float
```
## Console

```python
print('Hello world!')                      # outputs given String

myName = input()                           # reads next String

import random
random_number = random.randint(1, 20)      # generate random integer

print('Hello', end='')                     # disables the newline at end of print statement
print(' World')

print('cats', 'dogs', 'mice', sep=',')     # disables automatic space between values

print(round(2.665, 2))                     # rounding a float with round()

truncate(1324343032.324325235, 3)          # truncate a float with truncate()

```

## Flow

```python
if numberX < 5:                     # if statement
  print('NumberX is below 5')
 
while numberX < 5:                  # while statement
  print('NumberX is below 5')
  numberX = numberX + 1

while True:                         # infinite while loop
  print('Who are you?')
  name = input()
  if name != 'Joe':
    continue                        # continue breaks loop early and returns to start of while
  print('Hello Joe, what is the password?')
  password = input()
  if password == 'swordfish':
    break                           # ends loop and continues
print('Access granted.')

for x in range(5):
  print("hello, round: " + str(x) )
  
for person in persons:                              # Using for to loop through a list
  print(f"Hello {person}, nice to meet you.")
```

```python
if x < y:
  print("x is less than y")
elif x > y:
  print("x is greater than y")
else:
  print("x is equal to y")
 ```

## Error Catching

```python
def divide(num_1, num_2):
    try:
        return num_1 / num_2
    except ZeroDivisionError:
        print("Can't divide by zero.")
        
# An else block can be added to have a block that will run if no error
try:
    result = num_1 / num_2
except ZeroDivisionError:
    print("Can't  divide by zero.")
else:
    print(f"{num_1} / {num_2} = {result}")
    
# You can explicitly do nothing in event of exception with pass
try:
    with open(filename, encoding='utf-8') as f:
        contents = f.read() # Reads the entire contents of the file into one string
except FileNotFoundError:
    pass
else:
    words = contents.split()    # Splits that string into a list of strings (words)
```
## Program Structure

```python
# A module is a separate .py file that stores functions.

# Import a module and then use the functions in it by first referencing that module
import pizza_module
pizza_module.make_pizza("cheese", 15)

# Import a specific or a selection of functions from a module directly, and then call them directly
from pizza_module import make_pizza, cook_pizza

# Give a function an alias (to avoid naming conflicts or shorten name)
from pizza_module import make_pizza as mp

# Give a module an alias
import pizza as p

# Import all functions in module - can then use all functions directly but can 
# be problematic in large modules, may create naming conflicts
from pizza import *

```

## Files

```python
with open('pi_digits.txt') as file_object:   # `with` handles close() to prevent accidental corruption of file
  contents = file_object.read()              # `.read()` returns entire contents as one string
  
# The file object of a `with` is iterable, so it can be stepped through line by line as separate strings    
with open('pi_digits.txt') as file_object:
    for line in file_object:                 
        print(line)
        
# The `file_object` is only accessible in the `with` block as it needs to be `open()` and `close()`'d. 
# Use `readlines()` to save all the lines in a list that will be available outside the `with` block
with open(filename) as file:
    lines = file.readlines()

for line in lines:
    print(line)
    
# By default, open(filename) opens the file in `read` mode. If you want to write to a file you can
# use `open(filename, 'w')` to allow you to write to a file.
with open(filename, 'w') as file_object:
  file_object.write("This is a new string.")
  
# Note that writing to a file will destroy an old file and create a new one each time, or create a new file
# if none exists. To add to an existing file you must use the append mode of open
with open(filename, 'a') as file_object:
  file_object.write("Text to be added to a file.")
```
