
# Data Types

In Python, data types can be classified into two broad categories: primitive types (also known as primitive data types) and non-primitive types (also known as composite or derived data types).

## Primitive Types:

Primitive types in Python are the fundamental data types that are not composed of other data types. They are built-in and directly supported by the language. The primitive types include:

- Numeric types: `int`, `float`, `complex`
- Text type: `str`
- Boolean type: `bool`

- Primitive types are immutable, which means their values cannot be changed once they are assigned.

## Non-Primitive Types:

Non-primitive types are data types that are composed of multiple primitive or non-primitive types. They are also known as composite or derived data types. Some common non-primitive types include:

- Sequence types: `list`, `tuple`, `range`
- Mapping type: `dict`
- Set types: `set`, `frozenset`

Non-primitive types are generally mutable, meaning their values can be modified after they are created.

# Data Types

- Data Type represent the type of data present inside a variable.
- In Python we are not required to specify the type explicitly. Based on value provided,the 
type will be assigned automatically.Hence Python is Dynamically Typed Language.

Python contains the following inbuilt data types
  1. int
  2. float
  3. complex
  4. bool
  5. str
  6. bytes
  7. bytearray
  8. range
  9. list
  10. tuple
  11. set
  12. frozenset
  13. dict
  14. None

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/584b9b1a-67b5-48e6-b353-b63369dfc49a)


`Note:` Python contains several inbuilt functions
1. ctype()
 to check the type of variable
 
2. id()
 to get address of object
 
3. print()
 to print the value
 
- In Python everything is object

##  int data type:

We can use int data type to represent whole numbers (integral values)
- Eg:
   ```
   >>>  a=10
    >>> type(a) #int
   ```

`Note:`
- In Python2 we have long data type to represent very large integral values.
- But in Python3 there is no long type explicitly and we can represent long values also by 
using int type only.

We can represent int values in the following ways
1. Decimal form
2. Binary form
3. Octal form
4. Hexa decimal form

 - `Decimal form(base-10):`
It is the default number system in Python
The allowed digits are: 0 to 9
Eg: a =10

- `Binary form(Base-2):`
The allowed digits are : 0 & 1
Literal value should be prefixed with 0b or 0B
Eg:
```
a = 0B1111
 a =0B123
 a=b111
 ```
 
 - `Octal Form(Base-8):`
The allowed digits are : 0 to 7
Literal value should be prefixed with 0o or 0O.

Eg: 
```
a=0o123
a=0o786
```
 
 - `Hexa Decimal Form(Base-16):`
The allowed digits are : 0 to 9, a-f (both lower and upper cases are allowed)
Literal value should be prefixed with 0x or 0X
Eg:
```
 a =0XFACE
 a=0XBeef
 a =0XBeer
 ```
 
- `Note:` Being a programmer we can specify literal values in decimal, binary, octal and hexa 
decimal forms. But PVM will always provide values only in decimal form.
```
 >>> a=10
 >>> b=0o10
 >>> c=0X10
 >>> d=0B10
 >>> print(a)  #output 10
 >>> print(b)  #output 8
 >>> print(c)   #output 16
 >>> print(d)   #output 2
```

## Base Conversions

- Python provide the following in-built functions for base conversions

1.`bin():`
We can use bin() to convert from any base to binary
Eg:
```
  >>> bin(15)   #output '0b1111' 
  >>> bin(0o11)  #output '0b1001' 
  >>> bin(0X10)  #output '0b10000' 
```
2. `oct():`
We can use oct() to convert from any base to octal
Eg:
```
 >>> oct(10) #output '0o12' 
 >>> oct(0B1111) #output '0o17' 
  >>> oct(0X123) #output '0o443' 
```
3. `hex():`
We can use hex() to convert from any base to hexa decimal
Eg:
```
 >>> hex(100) #output '0x64' 
 >>> hex(0B111111) #output '0x3f' 
 >>> hex(0o12345) #output '0x14e5' 
```
## float data type:
We can use float data type to represent floating point values (decimal values)
Eg:
```
 >>> f=1.234 
 >>> type(f) #output float
 ```
We can also represent floating point values by using exponential form (scientific notation)
Eg:
 ```
 >>> f=1.2e3
 >>> print(f) #output 1200.0 
 ```
- instead of 'e' we can use 'E'
- The main advantage of exponential form is we can represent big values in less memory.
***Note:
We can represent int values in decimal, binary, octal and hexa decimal forms. But we can 
represent float values only by using decimal form.
Eg:
```
 >>> f=0B11.01 
 File "<stdin>", line 1 
 >>> f=0B11.01
  ^ 
 SyntaxError: invalid syntax 

 >>> f=0o123.456 
 SyntaxError: invalid syntax 
 
 >>> f=0X123.456 
 SyntaxError: invalid syntax 


```

## Complex Data Type:
A complex number is of the form.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/1402ef57-5b44-40e3-ab89-65c29e43f47a)

- a and b contain integers or floating point values
-  Eg:
   - 3+5j
   - 10+5.5j
   - 0.5+0.1j
   
- In the real part if we use int value then we can specify that either by decimal,octal,binary 
or hexa decimal form.
- But imaginary part should be specified only by using decimal form.
```
 >>> a=0B11+5j 
 >>> a 
   (3+5j) 
 >>> a=3+0B11j 
 SyntaxError: invalid syntax 
 ```
 ```
Even we can perform operations on complex type values.
 >>> a=10+1.5j 
 >>> b=20+2.5j 
 >>> c=a+b 
 >>> print(c) 
 (30+4j) 
 >>> type(c) 
 <class 'complex'> 
```

- `Note:` Complex data type has some inbuilt attributes to retrieve the real part and 
- ** imaginary part **
```
c=10.5+3.6j
c.real==>10.5
c.imag==>3.6
```

- We can use complex type generally in scientific Applications and electrical engineering 
Applications.


## bool data type:

- We can use this data type to represent boolean values.
- The only allowed values for this data type are:
`True and False`
- Internally Python represents True as 1 and False as 0
``
b=True
type(b) =>bool
``
Eg:
```
 >>> a=10
 >>> b=20
 >>> c=a<b
 >>> print(c)==>True
 >>> True+True==>2
 >>> True-False==>1
```
## str type:

- str represents String data type.

- A String is a sequence of characters enclosed within single quotes or double quotes.
```
s1='durga'
s1="durga"
```
- By using single quotes or double quotes we cannot represent multi line string literals.
```
s1="durga

soft"
```
- For this requirement we should go for triple single quotes(''') or triple double quotes(""")
```
s1='''durga
 soft'''
s1="""durga
 soft"""
 ```
- We can also use triple quotes to use single quote or double quote in our String.

```
''' This is " character'''
' This i " Character '
```
- We can embed one string in another string
```
'''This "Python class very helpful" for java students'''
```
## Slicing of Strings:
- slice means a piece
- [ ] operator is called slice operator,which can be used to retrieve parts of String.
- In Python Strings follows zero based index.
- The index can be either +ve or -ve.
- +ve index means forward direction from Left to Right
- -ve index means backward direction from Right to Left

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/a67b0cba-073e-48f7-9806-412f9d239447)


```
>>> s="durga" 
>>> s[0] 
 'd' 
 >>> s[1] 
 'u' 
 >>> s[-1] 
 'a' 
 >>> s[40] 
IndexError: string index out of range

>>> s[1:40] 
'urga' 
 >>> s[1:] 
 'urga' 
 >>> s[:4] 
 'durg' 
 >>> s[:] 
 'durga' 
 >>> s*3 
 'durgadurgadurga'  
 >>> len(s) 
   5
```

`Note:`
1. In Python the following data types are considered as Fundamental Data types
    - int 
    - float
    - complex
    - bool
    - str
2. In Python,we can represent char values also by using str type and explicitly char type is 
not available.
Eg:
```
>>> c='a' 
>>> type(c) 
  <class 'str'> 
```
3. long Data Type is available in Python2 but not in Python3. In Python3 long values also 
we can represent by using int type only.
4. In Python we can present char Value also by using str Type and explicitly char Type is 
not available. 

## Type casting






