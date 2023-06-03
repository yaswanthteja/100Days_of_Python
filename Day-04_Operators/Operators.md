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






## Operator precedence



![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/8920784a-4d80-46b2-be3e-6b2992cc87fa)


