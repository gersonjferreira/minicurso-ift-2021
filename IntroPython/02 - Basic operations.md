# Introduction to Phyton

This is a very simple and limited set of examples for those using python for the first time. For more detail, please check online tutorials. My favorites are:

https://www.w3schools.com/python/default.asp

https://www.tutorialspoint.com/python/index.htm

https://compphysics.readthedocs.io/

-------------------------

## Basic operations

**1) Assignment**


```python
a = 3
b = 4
c = a**2 + b**2
print('c = ', c)
```

**2) If / else statements**


```python
if a > b:
    print('a is larger than b')
elif a < b:
    print('b is larger than a')
else:
    print('a is equal to b')
```

**3) Types of variables and floating point imprecision**


```python
x = 5         # int
y = 4.2       # float
Na = 6.022e23 # float
z = 3 + 4j    # complex
a = 'hello'   # string

print(type(z))
```

Always remember that **floats** are binary approximations of real numbers. What is the big difference between these two examples below?


```python
# EXAMPLE 1:
x = 0.1
y = 3*x
z = 0.3

print('Is z == 0.3?', z == 0.3)
print('Is z == y?', z == y)
```


```python
# EXAMPLE 2:
x = 0.25
y = 3*x
z = 0.75

print('Is z == 0.75?', z == 0.75)
print('Is z == y?', z == y)
```

**SOLUTION:**

In the first example, 0.1 is a *repeating fraction* in base 2, which reads 

- (0.1)$_b$ = 0.0001100110011... 

If we truncate it at these decimals, it would read back in base 10 as 

- (0.0001100110011)$_{10}$ = 0.0999755859375

On the other hand, 0.25 = $2^{-2}$, which is exact in base 2 and reads as (0.25)$_b$ = 0.01

Therefore, the correct comparison between **floats** is


```python
small_number = 1e-12 # small enough be be considered zero

# EXAMPLE 1:
x = 0.1
y = 3*x
z = 0.3

print('1) Is z == y?', abs(z-y) < small_number)

# EXAMPLE 2:
x = 0.25
y = 3*x
z = 0.75

print('2) Is z == y?', abs(z-y) < small_number)
```

**4) Operators**

Arithmetic: + , - , * , /

Exponentiation: **
- ex: `1024 == 2**10`

Assignment: = , += , -= , *= , /=
- ex: `x *= 3 → x = x*3`

Comparison: ==, !=, >, >=, <, <=

Logical: `and , or , not`

Membership: in , not in
- ex: `5 in [3, 2, 9]` → False

Other useful: % (modulus), // (floor division)
- ex: `17 // 3` → 5
- ex: `17  % 3` → 2

**5) Lists**


```python
fruits = ['bananas', 'oranges']
fruits.append('apples')
fruits = fruits + ['grapes']
fruits.sort()

print('Length:', len(fruits))
print('first:', fruits[0])
print('last:', fruits[-1])
```

**6) For loops over lists**


```python
for fruit in fruits:
    print('we have', fruit)
```

**7) Membership**


```python
if 'grapes' in fruits:
    print('yes, we have grapes')
else:
    print('no, we don’t have grapes')
```

**8) List over range of integers**

Syntax:
- range(n) → 0,1,..n-1
- range(a, b, s) → semi-open interval (a,b] with steps s


```python
for i in range(3, 15, 2):
    print(i)
```


```python
for i in range(len(fruits)):
    print(i, fruits[i])
```

**9) Functions and docstrings**


```python
def bhaskara(a, b, c=0):
    '''
    Calculates the roots of ax²+bx+c=0.
    
    Input:
    ------
        a, b, c: (floats or integers)
        Coefficients of the quadratic polynomial. 
        If not given, c is assumed to be 0 just for this example.
        
    Output:
    -------
        x1, x2: (tuple of floats or complex)
        The roots x1 and x2.
    '''
    d = (b**2-4*a*c)**0.5
    x1 = (-b+d)/(2*a)
    x2 = (-b-d)/(2*a)
    return x1, x2

# calling the function
r1, r2 = bhaskara(1, -5, 6)
print('roots:', r1, ' and', r2)

# try now with calls to 
#   bhaskara(1, -5)
#   bhaskara(1, -5, 7.25)
```

**10) Lambda inline functions**


```python
def quadratic(a, x):
    return 5*a*x**2
    
square = lambda a, x: 5*a*x**2

print('The long form:', quadratic(1, 2))
print('The short form:', square(1, 2))
```

**11) Libraries**


```python
# importing a single function from a lib
from numpy import sqrt

print('Square root of 2 is', sqrt(2))

# importing the full lib and giving it an alias
import numpy as np

print('Square root of 4 is', np.sqrt(4))
```

**12) Comprehensions**

The comprehensions does not require *numpy*, but quite often we'll combine it with *numpy* for faster data manipulation (we'll discuss **numpy broadcast** later).


```python
# simple function to illustrate the calls
f = lambda i: i**2

# short loop notation to set a vector
avector = np.array([ f(i) for i in range(5) ])

print(avector)
```


```python
# is equivalent to this for loop
avector = np.zeros(5)
for i in range(5):
    avector[i] = f(i)

print(avector)
```


```python
# or even this one that starts with an empty list
avector = []
for i in range(5):
    avector += [f(i)]
avector = np.array(avector)

print(avector)
```


```python
# since we are talking about numpy already
# it can be also defined as
avector = f(np.arange(5)) # assuming f(i) is vectorizable

print(avector)
```


```python
# it can also be used to build matrices or tensors

# simple function to ilustrete
f = lambda i,j: i + j*1j

# loops run over columns first and then lines
columns = range(3)
lines = range(3)
amatrix = np.array([[f(i, j) for j in columns] for i in lines])

print(amatrix)
```


```python
# is equivalent to two nested loops
amatrix = np.zeros([3,3], dtype=complex)
for i in range(3):
    for j in range(3):
        amatrix[i, j] = f(i, j)

print(amatrix)
```

**13) Dictionaries**


```python
params = {}
params['temperature'] = 300
params['mag. field'] = 10
params['method'] = 'RK4'

print('List all params:', params)
print('T =', params['temperature'])
```

-------------------------
## Exercise: factorial

Write a function called `myfactorial` that uses a `for loop` to calculate the factorial $n!$

Your function should work as in the test code below:


```python
def myfactorial(n):
    f = 1
    #######################
    # YOUR CODE GOES HERE #
    #######################
    return f
    
# testing it
n = 10 # try it with different values
print('From numpy: ', np.math.factorial(n))
print(' Your code: ', myfactorial(n))
```
