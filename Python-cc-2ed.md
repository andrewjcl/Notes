# python-crash-course-notes
Notes for Python Crash Course 2nd Ed


```python
# Hello World!
print("Hello World")

# simple String functions
name = "Ada Lovelace"
print(name.title())
print(name.upper())
print(name.lower())

# f strings
first_name = "ada"
last_name = "lovelace"
full_name = f"{first_name} {last_name}"
print(full_name)

# Tabs and newlines
print("\tLet's put \nthis on a new line.")

# Strip of whitespace
favorite_language = "   python   "
print(favorite_language.lstrip())
print(favorite_language.rstrip())
print(favorite_language.strip())

# Numbers
3 ** 2          # Exponent
4 / 2           # Division always returns float
1 + 2.0         # Any operation with a float returns float
age = 10_000    # Underscore can be used for readability


# range()
for value in range(1, 5):   # range(a, b) generates a series of numbers
print(value)                # 1, 2, 3, 4 (excludes 5)

for i in range(2, 21, 2):   # range(start, end, step)
    print(i)                # 2, 4, 6, 8, , ..., 20

for i in range(10):         
    print(i)                # 0, 1, 2, 3, ..., 9





numbers = [1, 2, 3, 4, 5]
print(min(numbers)) 
print(max(numbers))
print(sum(numbers))

# Lists

"""
In python a list is a dynamically sized array. It need not be homogenous,
that is it can contain different types of objects.
Ordered
Mutable
Hetergeneous
Contains Duplicates
"""

# List Basics
bicycles = ['giant', 'trek', 'cannondale', 'bianchi']
print(bicycles[0])                  
print(bicycles[1].title())
bicycles.append('felt')            
bicycles.insert(1, 'pinarello')
del bicycles[1]                     
element = bicycles.pop()           
specific_element = bicycles.pop(3)  
bicycles.remove('trek')             # ONLY first occurence.


# Sorting
cars = ['honda', 'mazda', 'toyota', 'bmw']
cars.sort()                 # Sorts in place
cars.sort(reverse=True)     # Reverse sort
temp = cars.sorted()        # Returns a sorted list - original unchanged
print(cars.reverse())       # Returns list in reverse order >NOT sorted
len(cars)                   # Returns length of list

# Looping
for car in cars:            # iterates through list with a reference variable
    print(car)


# List Tricks
names = ['andrew', 'james', 'ling li', 'tutti']
last = names[-1]                            # Returns last element
third_last = names[-3]                      # Returns third last element
names.extend(['sally', 'troy'])             # Add multiple elements
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
first_three = letters.slice[:3]             # First 3 slice
new_slice = letters.slice[2:4]              # Two elements - index 2, 3
new_slice = letters.slice[:-5]              # From start, but not 5 at end
new_slice = letters.slice[-2:-2]            # Leave 2 at start and end
letters_2 = letters[:]                      # Element level copy
print('andrew' in names)                    # Checking if value in list

if user not in names:
    print(f"Sorry, {user} not found.")      # Checking if value not in list

if names:                                   # Checking if list is empty
    print("Not empty")
else:
    print("Empty")

# List comprehension - one line list creation using range
squares = [value ** 2 for value in range(1, 11)]

# List comprenesion - with additional check
squares_of_even = [value ** 2 for value in range(1, 11) if value % 2 == 0]


# Useful general functions
my_object.len()              # Length
my_object.str()              # String (toString)
my_object.type()             # Data type
animals.count('dog')         # Returns amount of times value appears in list

# Tuples

""" Tuples are ordered collections of heterogeneous data that are unchageable.
They can be accessed through indexing and slicing.
Ordered
Immutable
Heterogeneous
Contains Duplicates
 """

# Three ways of creating Tuples
tup_one = (1, 2, 'Andrew')
tup_two = tuple('Michael', [12, 13, 14], 6)
tup_three = 12, 14, 'Sally'

tuple1 = (10, 20, 30, 40, 50)
position = tuple1.index(30)         # Returning index for value
exists = 50 in tuple1               # Checking if value exists in tuple

# Dictionaries

""" 
Dictionaries are unordered collections of unique values stored
in Key-Value pairs.
Ordered - There is no index for items
Mutable
** Key - Must be immutable, must be unqiue (string, number or tuple)
** Value - Can by any type, can be duplicate
 """


person = {
    "andrew"  : "0411322586",
    "ling li" : "0413887277",
    "garry"   : "0412345678" 
}

print(person['andrew'])         # Works, but will throw error if not found
print(person.get('andrew'))     # Will safely return none if not found

person.keys()                   # Returns all keys as list
for key in person.keys():       # Prints all keys
    print(key)

person.values()                 # Returns all values as list
for value in person.values():   # Prints all values
    print(value)                

for item in person.items():     # Gives access to both key and value
    print(f"k: {item[0]} \tv: {item[1]}")

for key, value in person.items():     # Neater method
    print(f"k: {key} \tv: {value}")

for key, value in persons.items():

# We can add a new item to a dictionary by defining a value for a key
persons['lisa'] = '0422333444'

del persons['andrew']           # Removing an element from a dictionary

favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python'
}

if 'erin' not in favorite_languages.keys():
    print('Erin, please take the poll')

for name in sorted(favorite_languages.keys()):   # Iterating through dictionary in sorted order
    print(f"{name.title()}, thank you for taking the poll.")

print("Languages mentioned in the poll so far: ")  # Casting values list as set to get unique values
for language in set(favorite_languages.values()):
    print(f"\t{language}")


# User Input

user_name = input("Enter your name: ")
user_age = input("Enter your age: ")
user_age = int(user_age)             # input() always returns string, need to cast for int/float


# Loops

current_number = 0          # continue statement returns immediately to start of loop
while current_number < 10:
    current_number += 1
    if current_number % 2 == 0:
        continue
    print(current_number)       # this statement is not reached if number is even


# Functions

def greet_user(first_name, last_name):
    print(f"Hello {first_name} {last_name}")

greet_user(last_name='lim', first_name='andrew')        # Keyword argument can override the default 
                                                        # positional arguments

def describe_pet(name, type='cat'):
    print(f"{name} is a {type}.")

describe_pet('Tutti')                                   # Default value for a parameter



# We can have an optional parameter by having it as the last parameter
# in the list, and giving it a default value of empty. Than check to 
# see if not empty, and proceed accordingly

def get_name(first, last, middle=''):
    if middle:
        return f"{first.title()} {middle.title()} {last.title()}"
    else:
        return f"{first.title()} {last.title()}"

print(get_name('Andrew', 'Lim'))

# We can pass many arguments with *parameter. The function will create a
# tuple of all values received.

def make_pizza(*toppings):
    print(toppings)

def make_pizza(size, *toppings):        # This function receives one required positional argument and 
                                        # wil convert all additional values into a tuple

# Double asterix ** creates a dictionary of received values instead of a tuple. As such,
# it requires a list of key-value pairs to be received.

def build_profile(first, last, **user_info):
    print(f"User name: {first} {last}")
    for key, value in user_info.items():
        print(f"{key}: {value}")

build_profile('Andrew', 'Lim', city='Newcastle', age=34)
