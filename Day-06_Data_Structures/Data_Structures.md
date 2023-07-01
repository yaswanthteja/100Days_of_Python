# Data Structures:
Data structures are containers or ways to organize and store data in memory. They provide a way to group related data elements together and define the relationships between them. In Python, there are several built-in data structures, including:

- `Lists`: Ordered collection of items.
- `Tuples`: Ordered, immutable collection of items.
- `Dictionaries`: Collection of key-value pairs.
- `Sets`: Unordered collection of unique elements.
- `Arrays`: Homogeneous collection of items.
- `Linked Lists`, `Stacks`, `Queues`, `Trees`, etc. (implemented using classes and objects)

Data structures allow for efficient storage, retrieval, and manipulation of data. They provide different methods and operations to work with the data they contain.


# Collection Types
There are a number of collection types in Python. While types such as int and str hold a single value, collection
types hold multiple values.

## Lists
The list type is probably the most commonly used collection type in Python. Despite its name, a list is more like an
array in other languages, mostly JavaScript.

 In Python, a list is merely an ordered collection of valid Python values.

- If we want to represent a group of individual objects as a single entity where insertion 
= order preserved and duplicates are allowed, then we should go for List.
insertion order preserved.
- Duplicate objects are allowed
- heterogeneous objects are allowed.
- List is dynamic because based on our requirement we can increase the size and decrease 
the size.
- In List the elements will be placed within square brackets and with comma seperator.
- We can differentiate duplicate elements by using index and we can preserve insertion 
order by using index. Hence index will play very important role.
- Python supports both positive and negative indexes. +ve index means from left to right 
where as negative index means right to left

 A list can be created by enclosing values, separated by commas, in square brackets:
```
int_list = [1, 2, 3]
string_list = ['abc', 'defghi']
```
### Creation of List objects
 We can create empty list object as follows...
```
 list=[] 
 print(list) 
 print(type(list)) 

 Output 
 [] 
 <class 'list'> 
```
- A list can be empty:

```
empty_list = []
``` 
-  If we know elements already then we can create list as follows

```
list=[10,20,30,40]
```
- List  With dynamic input:

```
list=eval(input("Enter List:")) 
print(list) 
print(type(list)) 

output:
D:\Python_classes>py test.py 
Enter List:[10,20,30,40] 
[10, 20, 30, 40] 
<class 'list'> 
```

- List With list() function:
```
l=list(range(0,10,2)) 
print(l) 
print(type(l)) 

D:\Python_classes>py test.py 
[0, 2, 4, 6, 8] 
<class 'list'>
```

Eg:

```
s="python" 
l=list(s) 
print(l) 

D:\Python_classes>py test.py 
['p', 'y', 't', 'h', 'o','n'] 

```

- with split() function:
``` 
s="Learning Python is very very easy !!!" 
l=s.split() 
print(l) 
print(type(l)) 

D:\Python_classes>py test.py 
['Learning', 'Python', 'is', 'very', 'very', 'easy', '!!!'] 
<class 'list'> 
```
## Note: 
Sometimes we can take list inside another list,such type of lists are called nested lists.
```
[10,20,[30,40]]
```


- The elements of a list are not restricted to a single data type, which makes sense given that Python is a dynamic
language:
```
mixed_list = [1, 'abc', True, 2.34, None]
```


- A list can contain another list as its element:

```
nested_list = [['a', 'b', 'c'], [1, 2, 3]]
```





## Accessing List Elements

We can access elements of the list either by using index or by using slice operator(:)
1. By using index:
- List follows zero based index. ie index of first element is zero.
- List supports both +ve and -ve indexes.
- +ve index meant for Left to Right
- -ve index meant for Right to Left

  ![image](https://github.com/yaswanthteja/100Days_of_Python/assets/93423367/6bf1fcbd-feac-4663-96e8-075c2cc44415)

```
list=[10,20,30,40]
```

2. By using slice operator:

Syntax:
```
list2= list1[start:stop:step]
```
- start ==>it indicates the index where slice has to start
 default value is 0
- stop ===>It indicates the index where slice has to end
 default value is max allowed index of list ie length of the list
- step ==>increment value
 default value is 1

Eg:
```
n=[1,2,3,4,5,6,7,8,9,10] 
print(n[2:7:2]) 
print(n[4::2]) 
print(n[3:7]) 
print(n[8:2:-2]) 
print(n[4:100])
Output
D:\Python_classes>py test.py 
 [3, 5, 7] 
 [5, 7, 9] 
 [4, 5, 6, 7] 
 [9, 7, 5] 
 [5, 6, 7, 8, 9, 10]
 ```
 

- The elements of a list can be accessed via an index, or numeric representation of their position. Lists in Python are
zero-indexed meaning that the first element in the list is at index 0, the second element is at index 1 and so on:
```
names = ['Alice', 'Bob', 'Craig', 'Diana', 'Eric']
print(names[0]) # Alice
print(names[2]) # Craig
```
- Indices can also be negative which means counting from the end of the list (-1 being the index of the last element).
So, using the list from the above example:
```
print(names[-1]) # Eric
print(names[-4]) # Bob
```
- Lists are mutable, so you can change the values in a list:
```
names[0] = 'Ann'
print(names)
# Outputs ['Ann', 'Bob', 'Craig', 'Diana', 'Eric']
```
- Besides, it is possible to add and/or remove elements from a list:
- Append object to end of list with L.append(object), returns None.
```
names = ['Alice', 'Bob', 'Craig', 'Diana', 'Eric']
names.append("Sia")
print(names)
# Outputs ['Alice', 'Bob', 'Craig', 'Diana', 'Eric', 'Sia']
```





---

# Manipulating elements of List


## Differences between append() and insert():

1. append()

- We can use append() function to add element to the end of the list.

- In List when we add any element it will come in last i.e. it will be last element.


```
 n=[1,2,3,4,5] 
 n.insert(1,888) 
 print(n) 
 
Output:
 [1, 888, 2, 3, 4, 5] 
```

2. insert()

- We can use insert() function to add element at specified index.
- in List we can insert any element in particular index number

- Note: If the specified index is greater than max index then element will be inserted at last position. If the specified index is smaller than min index then element will be inserted at first position.

```
 n=[1,2,3,4,5] 
 n.insert(1,888) 
 print(n) 
 
 output:
 [1, 888, 2, 3, 4, 5] 
```

3.  extend() function:
- To add all items of one list to another list
- l1.extend(l2) 
 - all items present in l2 will be added to l1

```
order1=["Chicken","Mutton","Fish"] 
order2=["RC","KF","FO"] 
order1.extend(order2) 
print(order1) 

Output:
['Chicken', 'Mutton', 'Fish', 'RC', 'KF', 'FO'] 
```


4. remove() function:
- To remove specified item from the list
- We can use this function to remove specified item from the list.If the item present 
multiple times then only first occurrence will be removed.

```
 n=[10,20,10,30] 
 n.remove(10) 
 print(n) 
 
 Output:
 [20, 10, 30] 
```

5. pop() function:
It removes and returns the last element of the list.
This is only function which manipulates list and returns some element.
Eg:
```
n=[10,20,30,40] 
print(n.pop()) 
print(n.pop()) 
print(n) 

D:\Python_classes>py test.py 
40 
30 
[10, 20] 
the list is empty then pop() function raises IndexError
```


Note:
1. pop() is the only function which manipulates the list and returns some value
2. In general we can use append() and pop() functions to implement stack datastructure 
by using list,which follows LIFO(Last In First Out) order.
In general we can use pop() function to remove last element of the list. But we can use to remove elements based on index.
- n.pop(index)===>  To remove and return element present at specified index.
- n.pop()==> To remove and return last element of the list.

## Differences between remove() and pop()

## remove():

1) We can use to remove special element
from the List. 
2) It can’t return any value.
3) If special element not available then we
get VALUE ERROR.


## pop():

1) We can use to remove last element
from the List.
2) It returned removed element.

3) If List is empty then we get Error.

Note:
- List objects are dynamic. i.e based on our requirement we can increase and decrease the size.
- append(),insert() ,extend() ===>for increasing the size/growable nature
- remove(), pop() ======>for decreasing the size /shrinking nature

