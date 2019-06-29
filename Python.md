# Python

[Structure](#structure)\
[Data](#data)\
[Console](#console)\
[Flow](#flow)

```
http://automatetheboringstuff.com/chapter1/
```
## Structure
*Flow*
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




*Operators*
```python
2 ** 3    # exponent            2 ** 3 = 8
22 // 8   # floored quotient   22 // 8 = 2
22 % 8    # modulus             22 % 8 = 6
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
```

## Flow



*For*

*While*

*Switch*

