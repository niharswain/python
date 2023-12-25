# Data Types:
    - fundamental data types
    - Classes : custoem type
    - Specialised Dat atypes: these are not inbuilt int python and can be installed in terms of modules
    - None

## Fundamental Data types:
    - int
    - float
    - bool
    - str
    - list
    - tuple
    - set
    - dict
    - complex & bin ()
    

### complex & bin ()
 - bin returns the binary repesentation of any object
 - any integer and float get stored in memory as binary


```python
print(bin(5))
```

    0b101
    


```python
print(bin(3+7))
```

    0b1010
    

# int & float


```python
# Int & float
# int is number
# float is decimal point
# you can use type to get the data type details
print (type(2))
print(type(5*1.5))
```

    <class 'int'>
    <class 'float'>
    


```python
#Addition of number
print(2+4)
```

    6
    


```python
#substarction 
print(2-4)
```

    -2
    


```python
#multiplictaion
print(2*4)
```

    8
    


```python
#Divide
print(4/2)
print(2/4)
```

    2.0
    0.5
    


```python
#double devide : result gets rounded down to integer
print(4//2)
print(2//4)
```

    2
    0
    


```python
#power of
print(2**2)
print(2**3)
```

    4
    8
    


```python
#modulo : modulo is the remainder of teh devision
print(4%2)
print(2%4)
print(5%2)
```

    0
    2
    1
    

### Math function


```python
#rounding number
print(round(3.1))
```

    3
    


```python
#abs: returns the actual value of an argument
print(abs(-20))
```

    20
    

### Operator Precedence


```python
print(20+3*2)
```

    26
    


```python
print(20-5*2)
```

    10
    


```python
print(10*2-2)
```

    18
    

#### Python follow below orders
    ()
    **
    * / 
    + - 

# Variables
    - assignig avlaue is called biniding
    - once we bind any value to any variable, we can use that variable anywhere in the programme 
    
##### How we should define varibale
    - start with lowercase or underscore (hello_world   or _world)
    - a varibal is case sensitive
    - There are keywords in python, we will not be able to define variable with same name as keyword
    - python Key word refernces:  https://www.w3schools.com/python/python_ref_keywords.asp



```python
a=10
iq=105
print (a)
print (iq)
```

    10
    105
    


```python
_iq=90
print(_iq)
```

    90
    


```python
a,b,c=10,2,30
print(a)
print(b,c)
```

    10
    2 30
    

##  Constant
    - contast value will never change
    - in variable we can change the value of the variable by re assigning.
    - you can write a constant by capital letters. Any varibale named in capital letters shows that it is a constant and you sould not change it.


```python
NAME='Nihar'
NAME="SWAIN"  # you can reassign the value, but as a best practice, you should not do it as its in capital letters and shows as constant.
PI=3.14
print (NAME)
print(PI)

print (NAME)
```

    SWAIN
    3.14
    SWAIN
    

### Expression vs Statements 
    - whole line is called statement
    - expression is used in statement
    
    user_age = iq/5   : this whole line is called statement & i1/5 is called expression
    iq=20  : this is statemnet
   

### Augmented assignment operator

    +=
    -=
    *=
    /=



```python
some_value=5
some_value=5+2
print(some_value)
# or you can do it as 

some_value=5
some_value=some_value+2
print(some_value)

#instead of doing it you can use augmented assignment operator
some_value=5
some_value+=2
print(some_value)

some_value-=2
print(some_value)
```

    7
    7
    7
    5
    


```python
some_value=10
some_value *=2
print(some_value)
```

    20
    


```python
another_value+=2
print(another_value)  # it shows error as we have defined the varibale another_value
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[58], line 1
    ----> 1 another_value+=2
          2 print(another_value)
    

    NameError: name 'another_value' is not defined


# Strings


```python
print (type("hello, how are you"))
```

    <class 'str'>
    


```python
# We can write string in below ways
username='Nihar'
password="123secret"

# long string can be written as below , it starts and end with '''   
long_string='''
wow
o o
---
'''

print (username)
print(password)
print(long_string)
```

    Nihar
    123secret
    
    wow
    o o
    ---
    
    

##### string operations

    - string concatenation
    - it means adding string together
    - string concatenation works only with string to string , not with string to integer 


```python
# string concatenation
# it means adding string together
# string concatenation works only with string to string , not with string to integer 

firstname='NIHAR'
lastname='SWAIN'
fullname= firstname + lastname

print (fullname)

print(firstname + ' ' +lastname)
```

    NIHARSWAIN
    NIHAR SWAIN
    

###### Type conversion

    - it would onvert one type of variable to another
    - we know 100 is an integer, but if we use str(100) , thats converts to str


```python
print(type(str(100)))
```

    <class 'str'>
    


```python
print(type(int(50.5)))
```

    <class 'int'>
    


```python
a=str(100)
b=int(a)
c=type(b)
print(c)
```

    <class 'int'>
    

##### Escape sequence 
    - we can use \ for escape sequence
    - python treats everything after \ as string
    - \t means tab
    - \n new line


```python
weather = "it's a "kind" of sunny"   # we have used ""  inside ""
print (weather)
```


      Cell In[75], line 1
        weather = "it's a "kind" of sunny"
                           ^
    SyntaxError: invalid syntax
    



```python
# \
weather="it's a \"kind\" of sunny"
print (weather)
```

    it's a "kind" of sunny
    


```python
# \t space
weather="it's a \"kind\" of \t sunny"
print (weather)
```

    it's a "kind" of 	 sunny
    


```python
# \n new line
weather="it's a \"kind\" of \n sunny"
print (weather)
```

    it's a "kind" of 
     sunny
    

##### formatted strings


```python
name='john'
age = 55
print('hi' + name + '. You are ' + str(age) + 'years old')
```

    hijohn. You are 55years old
    

##### in staed of doing above you can do formatted string 
    - when you mention f in the begining, python treats as formatted string


```python
name='John'
age=55
print(f'hi {name}. you are {age} years old')
```

    hi John. you are 55 years old
    

##### Instead of writting f in the begining, there is another way to write formatted string (not recomended)
    - print('statement'.format())


```python
name='john'
age=55
print('hi {}. You are {} years old'.format('John', '55'))
```

    hi John. You are 55 years old
    


```python
name='john'
age=55
print('hi {}. You are {} years old'.format(name, age))
```

    hi john. You are 55 years old
    


```python
name='john'
age=55
print('hi {1}. You are {0} years old'.format('John', '55')) # it would take variable in position 1 first and 0 second
```

    hi 55. You are John years old
    

#### String Indexes

    name='India'
          01234

    indexing works as below way of slicing
    [start:stop:stepover]


```python
name='India'
string_number='012345678'  # to understand the index concept

print(name[0])
print(string_number[5])
```

    I
    5
    


```python
name='India'
string_number='012345678'

print(name[0:2])  # it will print position of 0,1 
print(string_number[1:5])  # it will print position of 1,2,3,4

```

    In
    1234
    


```python
name='India'
string_number='012345678'

print(name[0:2])  # it will print position of 0,1 . starts at 0 and stops before 2
print(string_number[1:5])  # it will print position of 1,2,3,4 . starts at 1 and stops before 5
```

    In
    1234
    


```python
name='India'
string_number='012345678'

print(name[0:5:1])  # it will print position of 0,1,2,3,4,5 . starts at 0 and stops before 5 and steps to next 1 position
print(string_number[1:7:2])  # it will print position of 1..3..5 . starts at 1 and stops before 7 and steps to next 2nd position
```

    India
    135
    


```python
name='India'
string_number='012345678'

print(name[0:])  # it will print position from 0 to end

print(string_number[1:])  # it will print position from 1 to end

print(name[:5])  # it will print position till 5

print(string_number[:6])  # it will print position till 6
```

    India
    12345678
    India
    012345
    


```python
name='India'
string_number='012345678'

print(name[:-1])  # it will print position but not the last one. -1 represents the last index

print(string_number[:-3])  # it will print position except last 3

print(name[::-1])  # it will print position in reverse order

print(string_number[::-2])  # it will print all the position by stepping over from last index
```

    Indi
    012345
    aidnI
    86420
    

#### Immutability
    - string in python are immuatable, that means you can reassign a new value to a varibale but you can not change the string
    



```python
name='india'
print(name) 

name='Ind' # you can re-assign a value
print(name)

name[0]='I'   # you can not not change the value

```

    india
    Ind
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[114], line 7
          4 name='Ind' # you can reassign a value
          5 print(name)
    ----> 7 name[0]='I'
    

    TypeError: 'str' object does not support item assignment


# Built-in Functions & Methods
    - while len(quote) is a built in function
    - quote.upper() is a built in method
    - https://www.w3schools.com/python/python_ref_string.asp


```python
#built-in functions in str
print(len('helooooo'))
```

    8
    


```python
greet='helloooo'
print(greet[0:len(greet)])
```

    helloooo
    


```python
# build in methods in string
quote='to be or not to be'
a=quote.upper()
print(a)
```

    TO BE OR NOT TO BE
    


```python
quote='to be or not to be'
a=quote.capitalize()
print(a)
```

    To be or not to be
    


```python
quote='to be or not to be'
a=quote.find('be')
print(a)

```

    3
    

# booleans
    - a boolean can be true or false
    - They are logical values
    - in boolean 1 means True
    - in boolean 0 means False


```python
name='John'
is_cool=False

is_cool=True

```


```python
print(bool(1))
```

    True
    


```python
print(bool(0))
```

    False
    

## Excercises : calculate age of a person


```python
# input() method used to get input 
# input converts the data in string by default. So you have to convert the data as per your requirement
import datetime
birth_year = input('what year you born')
current_year=datetime.date.today().year
age=current_year-int(birth_year)
print(f'you are born in {birth_year} and your age is {age}')
```

    what year you born2000
    you are born in 2000 and your age is 23
    

# Commenting rules in python
       - comments shuld be self explanatory
       - it should be understandable by other developers
       - https://realpython.com/python-comments-guide/


```python
# programme to greet with user name and tell the length of the password
user=input('Type your username')
pwd=input('Type your password')
pwd_length=len(pwd)
pwd_st='*' * pwd_length
print (pwd_st)
print(f'Hello {user}, Your password {pwd_st} is {pwd_length} letters length')
```

    Type your usernameNihar
    Type your passwordhello world
    ***********
    Hello Nihar, Your password *********** is 11 letters length
    

# List [   ]
    - list would be declared inside a [square bracket]
    - li = [1,2,3,4,5]
    - li = ['a','b','c']
    - li = [1,2,'a',True]
    - List is a collection of array and can be of any data type
    - List is mutable, that means you can chnage the value inside list


```python
amazon_cart = ['notebooks','sunglasses']
print(amazon_cart[0])
```

    notebooks
    

##### List Slicing
    - 


```python
amazon_cart=[
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]
print(amazon_cart)

# list is mutable
amazon_cart[0]='laptop'
print(amazon_cart)


```

    ['notebooks', 'sunglasses', 'toys', 'grapes']
    ['laptop', 'sunglasses', 'toys', 'grapes']
    

##### copying & modifying a list to another list   *** Important ***


```python
amazon_cart=[
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]
print(amazon_cart) 

new_cart=amazon_cart # but this not the right way
new_cart[0]='pen' # assigned a new value to position 0 
print(new_cart)
print(amazon_cart)   # here you can see amazon_cart is also got changed with a new value for position 0
```

    ['notebooks', 'sunglasses', 'toys', 'grapes']
    ['pen', 'sunglasses', 'toys', 'grapes']
    ['pen', 'sunglasses', 'toys', 'grapes']
    


```python
amazon_cart=[
    'notebooks',
    'sunglasses',
    'toys',
    'grapes'
]
print(amazon_cart) 

new_cart=amazon_cart[:] # this is the correct way 
new_cart[0]='pen' # assigned a new value to position 0 
print(new_cart)
print(amazon_cart)   # here you can see amazon_cart has not changed
```

    ['notebooks', 'sunglasses', 'toys', 'grapes']
    ['pen', 'sunglasses', 'toys', 'grapes']
    ['notebooks', 'sunglasses', 'toys', 'grapes']
    

#### Matrix
    - A matrix is a way to describe a multi dimensional list
    - Its a array with another array inside it
    


```python
matrix_example=[
    [1,2,3],
    [4,5,6],
    [7,8,9]
]

print(matrix_example)

print(matrix_example[0][1])  # row: 0   coloumn:1
```

    [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
    2
    

##### List methods


```python
basket=[1,2,3,4,5]
print(len(basket))
```

    5
    


```python
# Adding
basket=[1,2,3,4,5]
new_basket=basket.append(100)  # it would not create a new list, it will add 100 in  basket
print(basket)    # 100 will be added
print(new_basket) # it will show None
```

    [1, 2, 3, 4, 5, 100]
    None
    


```python
# Adding
basket=[1,2,3,4,5]
basket.append(100)  #it will add 100 in  basket
new_basket=basket  # new basket will be crated as per basket
print(basket)    # 100 will be added
print(new_basket) # list like basket
```

    [1, 2, 3, 4, 5, 100]
    [1, 2, 3, 4, 5, 100]
    


```python
# Insert(index,object)
basket=[1,2,3,4,5]
basket.insert(4,100)  #it will add 100 in  4 th positon 
new_basket=basket  # new basket will be crated as per basket
print(basket)    # 100 will be added
print(new_basket) # list like basket
```

    [1, 2, 3, 4, 100, 5]
    [1, 2, 3, 4, 100, 5]
    


```python
# remove and pop
basket=[1,2,3,4,5]
basket.pop()  # remove last position
print(basket)    # 

basket.pop(2)  # remove 2nd position
print(basket)    # 

```

    [1, 2, 3, 4]
    [1, 2, 4]
    


```python
# removing
basket=[1,2,3,4,5]
basket.remove(4)  # remove the value 4
print(basket)    # 

basket.remove(2)  # remove the value 2
print(basket)    # 

```

    [1, 2, 3, 5]
    [1, 3, 5]
    

    - remove method removes the value, if you mention hi or bye or 7 or 8, it will just remove that
    - pop will remove the index postion, if you mention 0 or 1 or 19 or 31, it will remove the postion 0,1,19,31 of that list


```python
# know the index position
basket=['a','b','c','d','e']

print(basket.index('a'))  # display the postion of 'a'
print(basket.index('d'))  # display the postion of 'd'
```

    0
    3
    


```python
# know the list has any value
basket=['a','b','c','d','e']

print('d' in basket) # return boolean value if the value is present
print('x' in basket) # return boolean value if the value is present
print('i' in 'Nihar') # return boolean value if the value i  is present in Nihar
```

    True
    False
    True
    


```python
# count of a value
basket=['a','b','c','d','e']
print(basket.count('d'))   # how many times d is present in the list
```

    1
    


```python
# sort : it sorts the values in place, means it changes the list
basket=['f','g','a','b','c','d','e']

basket.sort()
print(basket)
```

    ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    


```python
# sorted : it sorts the values in a new list, it will not modify the original list
basket=['f','g','a','b','c','d','e']

print(sorted(basket)) # it will modify in  anew list
print(basket)  
```

    ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    ['f', 'g', 'a', 'b', 'c', 'd', 'e']
    


```python
# copy from one list to another list
basket=['f','g','a','b','c','d','e']
new_basket=basket.copy()
new_basket.sort()
print(new_basket)
print(basket)  
```

    ['a', 'b', 'c', 'd', 'e', 'f', 'g']
    ['f', 'g', 'a', 'b', 'c', 'd', 'e']
    


```python
# reverse
basket=['f','g','a','b','c','d','e']


basket.reverse() # it will reverse basket without sorting

print(basket)  
```

    ['e', 'd', 'c', 'b', 'a', 'g', 'f']
    


```python
basket=['f','g','a','b','c','d','e']

basket.sort()
basket.reverse() # it will reverse basket with sorting

print(basket)
```

    ['g', 'f', 'e', 'd', 'c', 'b', 'a']
    

#### Common List Patterns


```python
basket=['a','x','b','c','d','e','d']
basket.sort()
basket.reverse()
print(basket[::-1])    # reverse a list
print(basket)
```

    ['a', 'b', 'c', 'd', 'd', 'e', 'x']
    ['x', 'e', 'd', 'd', 'c', 'b', 'a']
    


```python
print(list(range(1,100)))
print(range(1,100))
```

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]
    range(1, 100)
    


```python
# join ()

sentence=''   # there is no space
new = sentence.join(['hi','my','name','is','Ram'])

print(new)
```

    hi my name is Ram
    


```python
# join ()

sentence=' '   # there is  space
new = sentence.join(['hi','my','name','is','Ram'])

print(new)
```

    hi my name is Ram
    


```python
# join ()

sentence='***'   # there is  ***
new = sentence.join(['hi','my','name','is','Ram'])

print(new)
```

    hi***my***name***is***Ram
    

#### List unpacking


```python
basket = [1,2,3]

a,b,c=[4,5,6]
d,e,f,*other,g=[1,2,3,4,5,6,7,8,9]
print(basket)
print(a)
print(b)
print(c)
print(other)
print(g)
```

    [1, 2, 3]
    4
    5
    6
    [4, 5, 6, 7, 8]
    9
    

# None

    - SOme of the out put dont produce something
    - None is a special data type in python 
    - a= None


```python
weapons=None
print(weapons)
```

    None
    

# dictionary

- dictionary is a data structure in python 
- dictionary is unorderd key value pair
-  A key has to be uniquie 


```python
dict={
    'a':1,
    'b':2,
    'c':3,
    'd':4
}

print (dict['b'])
print(dict)
```

    2
    {'a': 1, 'b': 2, 'c': 3, 'd': 4}
    


```python
dictionary={
    'a':[1,2,3],
    'b':'hello',
    'x':True
}


print (dictionary['a'][1])  # print dictionary --> key a ==> position 1 of key 1
print(dictionary['a'][2],['x'])
```

    2
    3 ['x']
    


```python
my_list=[
    {
    'a':[1,2,3],
    'b':'hello',
    'x':True
}
]

print(my_list[0]['a'][2])
```

    3
    


```python
dictionary={
    '123':[1,2,3],
    [100]:True,
    '123':'Hello'
}

print(dictionary[100])
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[21], line 1
    ----> 1 dictionary={
          2     '123':[1,2,3],
          3     [100]:True
          4 }
          6 print(dictionary[100])
    

    TypeError: unhashable type: 'list'



```python
user={
    'basket':[1,2,3],
    'greet':'Hello'
}

#print(user['age']) # show errors as age is not present as a key

print(user.get('age'))  # it wont show an error, it will show NONE as age as a key is not present.
print(user.get('age',55))  # it wont sow the error and in stead of NONE it will print 55 as default value
```

    None
    55
    


```python
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}

#print(user['age']) # show errors as age is not present as a key

print(user.get('age'))  # it wont show an error, it will show NONE as age as a key is not present.
print(user.get('age',55))  # it wont sow the error and in stead of NONE it will print 55 as default value if age is not present
```

    20
    20
    


```python
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}

print('size' in user)   # False as Size is not present as key
print('basket' in user)  # True as basket is present as key
print('age' in user.keys())   # true as age is present as akey
print('Hello' in user.values()) # True as Hello is present as value in the dictionary 
```

    False
    True
    True
    True
    


```python
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}

user.clear() # empty dictinary
print(user)   
```

    {}
    


```python
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}


user2=user.copy()
print(user) 
print(user2)
```

    {'basket': [1, 2, 3], 'greet': 'Hello', 'age': 20}
    {'basket': [1, 2, 3], 'greet': 'Hello', 'age': 20}
    


```python
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}

user2=user.copy()
print(user.clear()) 
print(user2)
```

    None
    {}
    


```python
#update a dictionary
user={
    'basket':[1,2,3],
    'greet':'Hello',
    'age':20
}
print(user.update({'ages':55}))
print(user)
```

    None
    {'basket': [1, 2, 3], 'greet': 'Hello', 'age': 20, 'ages': 55}
    

# Tuples
    - A tuple is a mutable list 
    - its less flexiblae
    - you cant sort
    - you cant reverse a tuple
    - its more performant than tuple
    - A dictionary return the key value as tuple


```python
my_tuple=(1,2,3,4,5)
print(my_tuple)  # print the tuple

print(5 in my_tuple)   # true is 5 is present in the tuple
```

    (1, 2, 3, 4, 5)
    True
    


```python
my_tuple=(1,2,3,4,5)
print(my_tuple)  # print the tuple

print(5 in my_tuple) 
```

    (1, 2, 3, 4, 5)
    True
    


```python
my_tuple=(1,2,3,4,5)
print(my_tuple)  # print the tuple

new_tuple=my_tuple[1:2]
print(new_tuple) 

new_tuple=my_tuple[1:4]
print(new_tuple) 
```

    (1, 2, 3, 4, 5)
    (2,)
    (2, 3, 4)
    


```python
my_tuple=(1,2,3,4,5)
print(my_tuple)  # print the tuple

x=my_tuple[1]
y=my_tuple[2]


print(x,y) 

a,b,c,*other=(1,2,3,4,5)  # here a,b,c is assigned to 1,2,3 and * others assigned to 4,5
print(other)
```

    (1, 2, 3, 4, 5)
    2 3
    [4, 5]
    

    - Tuple has two method count and index


```python
my_tuple=(1,2,3,4,5,6,7)

print(my_tuple.count(5))   # it will count how many 5 or values presentin the tuple

print(my_tuple.index(5))  # index of value 5

print(len(my_tuple))
```

    1
    4
    7
    

# Set
    - set is unordered list of unique object
    - set does not support indexing


```python
my_set={1,2,3,4,5,8,9}


print(my_set)

my_set.add(100)
my_set.add(2)  
print(my_set)  # only 100 will be seen , no duplictaion of 2
```

    {1, 2, 3, 4, 5, 8, 9}
    {1, 2, 3, 4, 5, 100, 8, 9}
    


```python
my_list=[1,2,3,4,5,5]

print(set(my_list))    # converts the list into set
```

    {1, 2, 3, 4, 5}
    


```python
my_set={1,2,3,4,5,8,9}


print(my_set)
print(1 in my_set)
print(len(my_set))
```

    {1, 2, 3, 4, 5, 8, 9}
    True
    7
    


```python
my_set={1,2,3,4,5,8,9,9}


print(list(my_set))     # converts into list

new_set=my_set.copy()
print(new_set)

print()
```

    [1, 2, 3, 4, 5, 8, 9]
    {1, 2, 3, 4, 5, 8, 9}
    


```python
my_set={1,2,3,4,5,8,9,9}

new_set=my_set.copy()
my_set.clear()   # empty the set
print(new_set)
print(my_set)
```

    {1, 2, 3, 4, 5, 8, 9}
    set()
    


```python
my_set={1,2,3,4,5,6}
your_set={4,5,6,7,8,9,10}

print(my_set.difference(your_set))  # diffrence()
print(my_set.discard(5))  # discard 5 or modify the set 
print(my_set)

print(my_set.difference_update(your_set))  # it will update the myset with the diffrence value
print(my_set)


```

    {1, 2, 3}
    None
    {1, 2, 3, 4, 6}
    None
    {1, 2, 3}
    


```python
my_set={1,2,3,4,5,6}
your_set={4,5,6,7,8,9,10}
any_set={11,12,13}

print(my_set.intersection(your_set))  # common 

print(my_set.isdisjoint(your_set))   # true if nothing in common , false if somehing is common
print(my_set.isdisjoint(any_set)) 


print(my_set.union(any_set))  # union just united both the sets by removing the duplicates 

```

    {4, 5, 6}
    False
    True
    {1, 2, 3, 4, 5, 6, 11, 12, 13}
    


```python
my_set={1,2,3,4,5,6}
your_set={4,5,6,7,8,9,10}
any_set={11,12,13}

print(my_set.intersection(your_set))  # common 
print(my_set & your_set)  # another way of intersection

print(my_set.union(any_set))  # union just united both the sets by removing the duplicates 
print(my_set | any_set) #another way of union 
```

    {4, 5, 6}
    {4, 5, 6}
    {1, 2, 3, 4, 5, 6, 11, 12, 13}
    {1, 2, 3, 4, 5, 6, 11, 12, 13}
    


```python
my_set={1,2,3,4,5,6}
your_set={4,5,6,7,8,9,10}
any_set={1,2,3}

print(my_set.issubset(any_set))
print(any_set.issubset(my_set))

print(my_set.issuperset(any_set))  # my set is superset of any_set. my_set is having more values that any_set
print(any_set.issuperset(my_set))
```

    False
    True
    True
    False
    


```python

```
