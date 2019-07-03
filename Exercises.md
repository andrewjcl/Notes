# Exercises

### Basic Input Output
---
```
Enter miles: ->96
96 miles is 153.6 kilometres
```
<details>
  <summary>Python - Complete</summary>

  ```python
  print('Enter miles: ')
  miles = float(input())
  kilometres = miles * 1.609
  print(f'{miles} miles is {round(kilometres, 1)} kilometres')
  ```
</details>

---
```
Enter length of the sides for equilateral triangle: ->3.5
The area is 3.89
```
<details>
  <summary>Python - Complete</summary>

  ```python
  import math

  print('Enter the length of the sides for equilateral triangle: ')
  side = float(input())
  area = math.sqrt(3) / 4.0 * side * side
  print(f'The area is {round(area, 2)}')
  ```
</details>

---
```
Enter a number between 0  and 1000: ->999
The multiplication of all digits in 999 is 729
```
<details>
  <summary>Python - Complete</summary>

  ```python
  print('Enter a number between 0 and 1000: ')
  input = input()

  total = 1

  for each in input:
      total *= int(each)

print(f'The multiplication of all digits in {input} is {total}')
  ```
</details>

---
```
Enter the number of minutes: ->1000000000
1000000000 minutes is approximately 1902 years and 214 days
```
<details>
  <summary>Python - Complete</summary>

  ```python
print('Enter the number of minutes: ')
minutes = int(input())

hours = minutes / 60
days = hours / 24
years = int(days / 365)

days_left_over = int(days - (years * 365))

print(f'{minutes} minutes is approximately {years} years and {days_left_over} days')
  ```
</details>

---
```
Enter the weight in kilograms: ->90
Enter the height in cm: -> 177
BMI is 31.0
```
<details>
  <summary>Python - Complete</summary>

  ```python
  print('Enter your weight in kg: ')
weight = float(input())

print('Enter your height in cm: ')
height = float(input()) / 100

bmi = weight / (height * height)

print(f'BMI is {round(bmi, 1)}')
  ```
</details>

---
```
Enter a number: -> 5
*
* *
* * *
* * * *
* * * * *
```
<details>
  <summary>Python - Complete</summary>

  ```python
print('Enter a number: ')
number = int(input())
star = '* '

for x in range(number + 1):
    print(star * x)
  ```
</details>

---
```
Enter a number: -> 5
1 : ODD
2 : EVEN
3 : ODD
4 : EVEN
5 : ODD
```
<details>
  <summary>Python - Complete</summary>

  ```python
def is_even(x):
    if x % 2 == 1:
        return False
    return True


print('Enter a number: ')
number = int(input())

for x in range(1, number + 1, 23):
    if is_even(x):
        print(f'{x} : EVEN')
    else:
        print(f'{x} : ODD')
  ```
</details>

---
```
Enter the driving distance (km): ->900
Enter litres per 100km: -> 9.5
Enter price per litre: -> 1.4
Enter your fuel tank capacity (litres): -> 63
Your range on full tank is:
Cost of full tank:
Cost and refills to drive Sydney to Perth:
```
<details>
  <summary>Python - Complete</summary>

  ```python
print('Enter the driving distance (km): ')
distance = int(input())

print('Enter the your mileage (L/100km): ')
mileage = 100 * 1 / float(input())  # Stored as km per Litre

print('Enter the price of fuel ($/Litre): ')
price = float(input())

print('Enter your fuel tank capacity (Litres): ')
capacity = int(input())

print('----------------------------------------')
print(f'\tYour range on full tank is {round(capacity * mileage)} km')
print(f'\tCost of a full tank is ${round(capacity * price, 2)}')
refills = int(3933.17 / (capacity * mileage)) + 1
fill_cost = price * capacity
print(f'\tCost and refills to drive Sydney to Perth is {refills} refills, total cost ${round(fill_cost * refills, 2)}')
  ```
</details>

---
```
Enter a number: -> 125
All prime numbers up to 125 are: 1, 3, 5, 7, ...
```
<details>
  <summary>Python</summary>

  ```python
  # answer here
  ```
</details>

---
```
Create a Bank object that has methods deposit(x), withdraw(x), and print_balance()
```
<details>
  <summary>Python - Complete</summary>

  ```python
  class Bank:

    balance = 0

    def __init__(self, name):
        self.name = name

    def deposit(self, amount):
        money_list = amount.split('.')
        dollars = int(money_list[0])
        cents = int(money_list[1])
        self.balance += ((dollars * 100) + cents)

    def withdraw(self, amount):
        money_list = amount.split('.')
        dollars = int(money_list[0])
        cents = int(money_list[1])
        self.balance -= ((dollars * 100) + cents)

    def print_balance(self):
        dollars = int(self.balance / 100)
        cents = (self.balance - (dollars * 100))

        if cents < 10:
            print(f'Current Balance: ${dollars}.0{cents}')
        else:
            print(f'Current Balance: ${dollars}.{cents}')


def main():
    bank01 = Bank("Andrew Lim")

    bank01.deposit("34.08")
    bank01.print_balance()
    bank01.deposit("0.80")
    bank01.print_balance()
    bank01.withdraw("5.20")
    bank01.print_balance()


if __name__ == "__main__":
    main()
  ```
</details>

---

