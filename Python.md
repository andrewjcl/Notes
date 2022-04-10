# Python

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
http://automatetheboringstuff.com/chapter1/
```
## Structure

*Defining a Function*
```python
def hello(argumentOne, argumentTwo):
  print(argumentOne + " " + argumentTwo)
```

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
def spam(divideBy):
    try:
        return 42 / divideBy
    except ZeroDivisionError:
        print('Error: Invalid argument.')
```
