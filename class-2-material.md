# Quadratic Expressions

```
import math

a = int(input("Enter value of a: "))
b = int(input("Enter value of b: "))
c = int(input("Enter value of c: "))
d = b*b - 4*a*c
if d < 0:
    print("ROOTS are imaginary")
else:
    root1 = (-b + math.sqrt(d)) / (2.0*a)
    root2 = (-b - math.sqrt(d)) / (2.0*a)
    print("Root 1 = ", root1)
    print("Root 2 = ", root2)
````

# Salesman Salary
````
basic_salary = 1500
bonus_rate = 200
commision_rate = 0.02
numberofcamera = int(input("Enter the number of inputs sold: "))
price = float(input("Enter the total prices: "))
bonus = (bonus_rate * numberofcamera)
commision = (commision_rate * numberofcamera * price)
print("Bonus        = %6.2f" % bonus)
print("Commision    = %6.2f" % commision)
print("Gross salary = %6.2f" % (basic_salary + bonus + commision))
````
