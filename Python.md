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
numbers[3:6]                                  # returns a new list 'slice', starting (inclusive) and ending (exclusive) index
numbers[:3]                                   # returns first 3 elements
numbers[-3:]                                  # returns last 3 elements


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
