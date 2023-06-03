# Operators

Operator is a symbol that performs certain operations.
Python provides the following set of operators

1. Arithmetic Operators
2. Relational Operators or Comparison Operators
3. Logical operators
4. Bitwise oeprators
5. Assignment operators
6. Special operators


## 1. Arithmetic Operators:


![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/eef397a8-c4ca-4398-94a1-644413e0ab57)

```
+ ==>Addition
- ==>Subtraction
* ==>Multiplication
/ ==>Division operator
% ===>Modulo operator
// ==>Floor Division operator
** ==>Exponent operator or power operator
```
Eg: test.py:

```
 a=10 
 b=2 
 print('a+b=',a+b) 
 print('a-b=',a-b) 
 print('a*b=',a*b) 
 print('a/b=',a/b) 
 print('a//b=',a//b) 
 print('a%b=',a%b) 
 print('a**b=',a**b)

 Output:
 Python test.py or py test.py 
 a+b= 12 
 a-b= 8 
 a*b= 20 
 a/b= 5.0 
 a//b= 5 
 a%b= 0 
 a**b= 100

```

Eg:
```
 a = 10.5 
 b=2 
 
 a+b= 12.5 
 a-b= 8.5 
 a*b= 21.0 
 a/b= 5.25 
 a//b= 5.0 
 a%b= 0.5 
 a**b= 110.25 

 ```
 
Eg:
```
10/2==>5.0
10//2==>5
10.0/2===>5.0
10.0//2===>5.0

```


- Note: / operator always performs floating point arithmetic. Hence it will always returns 
## float value.
- But Floor division (//) can perform both floating point and integral arithmetic. 
- If arguments are int type then result is int type. If atleast one argument is float type then result is float type.

Note:
We can use +,* operators for str type also.
If we want to use + operator for str type then compulsory both arguments should be str 
type only otherwise we will get error.
```
 >>> "python"+10 
 TypeError: must be str, not int 
 >>> "python"+"10" 
 'python10'
 ```

- If we use * operator for str type then compulsory one argument should be int and other argument should be str type.
```
2*"python"
"python"*2
2.5*"python" ==>TypeError: can't multiply sequence by non-int of type 'float'
"python"*"python"==>TypeError: can't multiply sequence by non-int of type 'str'
```
```
+  ====>String concatenation operator
*  ===>String multiplication operator
```

`Note:` For any number x,
x/0 and x%0 always raises "ZeroDivisionError"
10/0
10.0/0
...


## 2. Relational Operators or Comparison Operators in Python

A comparison operator is used to comparing two or more variables or constants having some values. We can compare different variables or constants in six different ways that include, comparing if two values are equal, or if two values are not equal, and many other ways.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/be4acfe1-a0f3-4461-a890-0078afb9c677)

## 3.Logical Operators in Python
The logical operator is used to perform some logical operations or combine conditional statements. Mainly logical operators are used in control statements like if, else, and elif where we can check more conditions together just by using these operators. Logical operators always return TRUE or FALSE values.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/82a18ed2-d97d-4bc4-bbab-8fe6fbe73308)


## 4. Bitwise Operators in Python

These operators are used to compare the binary numbers. We can perform different operations on binary numbers such as and, or, xor, not, left shift, and right shift. Sometimes these operators are also called bitwise-or, bitwise-and, and bitwise-xor and so on. Shift operators are used to shifting the values of the binary number to left or right.

- We can apply these operators bitwise.
- These operators are applicable only for int and boolean types.
- By mistake if we are trying to apply for any other type then we will get Error.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/36394d7e-483a-4198-ba07-1daf00528fa5)


```
& ==> If both bits are 1 then only result is 1 otherwise result is 0
| ==> If atleast one bit is 1 then result is 1 otherwise result is 0
^ ==>If bits are different then only result is 1 otherwise result is 0
~ ==>bitwise complement operator
 1==>0 & 0==>1
<< ==>Bitwise Left shift
>> ==>Bitwise Right Shift

example:

print(4&5) ==>valid
print(10.5 & 5.6) ==> TypeError: unsupported operand type(s) for &: 'float' and 'float'
print(True & True) ==>valid
print(4&5) ==>4
print(4|5) ==>5
print(4^5) ==>1
```
![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/1e1dabb3-8233-411d-9f7e-da809c501b45)

## bitwise complement operator(~):
- We have to apply complement for total bits.
Eg: print(~5) ==>-6
`Note:`
- The most significant bit acts as sign bit. 0 value represents +ve number where as 1 
represents -ve value.
- positive numbers will be repesented directly in the memory where as -ve numbers will be 
represented indirectly in 2's complement form.

# Shift Operators:
## << Left shift operator
- After shifting the empty cells we have to fill with zero

```
print(10<<2)==>40
``` 
![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/84fcdc79-0141-4f0e-bda4-e1d74ff52b61)

## >> Right Shift operator

- After shifting the empty cells we have to fill with sign bit.( 0 for +ve and 1 for -ve)
 ```
 print(10>>2) ==>2
 ```
 ![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/2ab471e6-dfb1-4244-8178-5f770db100f8)

We can apply bitwise operators for boolean types also
```
print(True & False) ==>False
print(True | False) ===>True
print(True ^ False) ==>True
print(~True) ==>-2
print(True<<2) ==>4
print(True>>2) ==>0
```

# Ternary Operator

The ternary operator, also known as the conditional expression, is a concise way to write simple conditional statements in Python. It follows the 
syntax: 
```
value_if_true if condition else value_if_false.
```

Example:

```
# Ternary Operator Example

# Input a number from the user
number = int(input("Enter a number: "))

# Check if the number is positive or negative using a ternary operator
result = "Positive" if number > 0 else "Negative"

# Print the result
print("The number is", result)

```


## Operator precedence



![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/8920784a-4d80-46b2-be3e-6b2992cc87fa)


# Special operators:
Python defines the following 2 special operators
1. Identity Operators
2. Membership operators

## 1. Identity Operators

Identity operators are used in Python programming language to check if the two values, variables, or constants are not only the same but also have the same memory location. These types of operators are used to compare and check the exact match of the values between two objects.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/91bb9d5e-92cc-44fb-aef4-2618a56cac45)


We can use identity operators for address comparison.
2 identity operators are available
1. is 
2. is not
- r1 is r2 returns True if both r1 and r2 are pointing to the same object
- r1 is not r2 returns True if both r1 and r2 are not pointing to the same object.



## Membership Operators in Python
Membership operators in python  are used for checking if the iterator or the given value is present in the sequence or not. These types of operators always return values in a TRUE or FALSE format. If the value is found in the sequence then the operator will return TRUE else the operator will return FALSE.

![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/597799f4-e95b-45de-aed5-4b24e532fc78)
