# Mathematical Functions (math Module)

A Module is collection of functions, variables and classes etc.
math is a module that contains several functions to perform mathematical operations

If we want to use any module in Python, first we have to import that module.
```
import math
```
Once we import a module then we can call any function of that module.
```
import math
print(math.sqrt(16))
print(math.pi)
4.0
3.141592653589793
```
We can create alias name by using as keyword.
```
import math as m
```
Once we create alias name, by using that we can access functions and variables of that module
```
import math as m
print(m.sqrt(16))
print(m.pi)
```
We can import a particular member of a module explicitly as follows
```
from math import sqrt
from math import sqrt,pi
```
If we import a member explicitly then it is not required to use module name while accessing.
``` 
from math import sqrt,pi
print(sqrt(16))
print(pi)
print(math.pi)  NameError: name 'math' is not defined
```

# important functions of math module:
```
ceil(x)
floor(x)
pow(x,y)
factorial(x)
trunc(x)
gcd(x,y)
sin(x)
cos(x)
tan(x)
....
```

important variables of math module:
```
pi  ===>3.14
e   ===>2.71 # eulers number
inf ==>infinity
nan ==>not a number
```

Q. Write a Python program to find area of circle
```
from math import pi
r=16
pi*r**2
print("Area of Circle is :",pi*r**2)
OutputArea of Circle is : 804.247719318987

```
