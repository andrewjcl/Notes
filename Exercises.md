# Exercises

### Basic Input Output
---
```
Enter miles: ->96
96 miles is 153.6 kilometres
```
<details>
  <summary><b>Python</b></summary>

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
  <summary><b>Python</b></summary>

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
  <summary><b>Python</b></summary>

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
  <summary>Python</summary>

  ```python
  # answer here
  ```
</details>

---
```
Enter the weight in kilograms: ->90
Enter the height in cm: -> 177
BMI is 31.0
```
<details>
  <summary><b>Python</b></summary>

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
  <summary>Python</summary>

  ```python
  # answer here
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
  <summary>Python</summary>

  ```python
  # answer here
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
  <summary>Python</summary>

  ```python
  # answer here
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
Make a selection 1) deposit, 2) withdraw, 3)check balance
multiple users?
history?
```
<details>
  <summary>Python</summary>

  ```python
  # answer here
  ```
</details>

---

