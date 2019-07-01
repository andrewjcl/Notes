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

*Casting*
```python
str(45)     # casting int to String 
int(1.25)   # casting float to int
float(10)   # casting int to float
```
## Console

```python
print('Hello world!')      # Outputs given String

myName = input()           # Reads next String

import random
random_number = random.randint(1, 20)     # Generate random integer


print('Hello', end='')     # Disables the newline at end of print statement
print(' World')

print('cats', 'dogs', 'mice', sep=',')  # Disables automatic space between values
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
```

```python
# In python 'for' is setup for use with iterators, but can still be used to run a set a mount
for x in range(5):
  print("hello, round: " + str(x) )
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
