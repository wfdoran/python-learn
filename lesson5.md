# Lesson 5

## Boolean Variables

Time to introduce a new variable type.

```python
x = 5 > 3
y = 5 > 8
z = 5 == 5
print(x,y,z)
print(type(x))
```

A boolean variable takes on the value `True` or `False` and
indicates whether an expression is correct.  The basic
comparison operations are given the following table.

| operator | description      | examples            |
| ---------| ---------------- | -----------------   |
| `==`     | equal            | `5 == 5` => `True`  |
|          |                  | `6 == 5` => `False` |
| `!=`     | not equal        | `6 != 5` => `True`  |
|          |                  | `5 != 5` => `False` |
| `>`      | greater than     | `7 > 3` => `True`   |
|          |                  | `7 > 7` => `False`  |
| `<`      | less than        | `7 < 8` => `True`   |
|          |                  | `7 < 1` => `False`  |
| `>=`     | greater or equal | `5 >= 5` => `True`  |
|          |                  | `5 >= 8` => `False` |
| `<=`     | less or equal    | `3 <= 6` => `True`  |
|          |                  | `3 <= 2` => `False` |

### Comparing Floats

All of comparisons above involve integers.  Things can get
more complicated with other variable types.

```python
print(0.33333333333333333333333 == 1/3)
print(0.33333333 == 1/3)
```

What happened here?  The precision of the floating point number
matters.  As general rule, you should not compare floats for
equality.  You can use less than and greater than without
worry, but equality is tricky.  Instead, test if two floats
are close to each other.

```python
print(1.000001 > 1.0)
print(0.999999 > 1.0)
print(abs(.333333 - 1/3)       < .00000001)
print(abs(.333333333333 - 1/3) < .00000001)
```

### Comparing Strings

```python
x = "hello"
y = "world"
print(x == y)
q = x + " " + y
z = "hello world"
print(q == z)
```

Two strings are the equal if they are the same length and 
contain exactly the same characters.  If they differ, the 
first character at whcih they differ is used to determine
which is greater.  This is call lexicographic ordering. 

```python
print("abc" > "aaa")
print("aaaa" > "aaa")
print("zzz" > "aaa")
print("ZZZ" > "aaa")
```

A funny thing about lexicographic ordering on most English
computer system, capital letters are smaller than lower-case 
letters.   

## if-then-else

You can use a boolean to "branch".  The code will follow a
different path based the whether the boolean expression is 
True or False.  

To understand the following code, remember that `i % 2` is 
`i` mod 2 or the remainder when you divide `i` by 2.  When
`i` is odd, the remainder is 1.  When `i` is even, the remainder 
is 0.

```python
for i in range(10):
    if i % 2 == 0:
        print(i, "is even")
    else:
        print(i, "is odd")
```


## Boolean Algebra

Boolean variables can be combined with the operations `and`, `or`, and `not`. 

```python
print(True and True)
print(True and False)
print(False and True)
print(False and False)
```

```python
print(True or True)
print(True or False)
print(False or True)
print(False or False)
```

```python
print(not True)
print(not False)
```

Putting it together, we can do things like add up all of the 
numbers less than 100 which are divisible by 2 or 7, but 
divisible by 14.

```python
total = 0
for i in range(100):
    if ((i % 2 == 0) or (i % 7 == 0)) and (not (i % 14) == 0):
        total += i
print(total)
```

You can show that [DeMorgan's Law](https://en.wikipedia.org/wiki/De_Morgan%27s_laws) which says `not (a or b)`
always equals `(not a) and (not b)`.

```python
for a in [True, False]:
    for b in [True, False]:
        left = not (a or b)
        right = (not a) and (not b)
        print(left, right)
```

## exercise 1 

Fill in the missing parts in the following code to produce a spiral.

```python
from turtle import *
reset()
edge_len = 50
for i in range(100):
    if (i % ___) == 0:
        edge_len = edge_len + ____
    forward(edge_len)
    right(___)
```

![sprial](https://github.com/wfdoran/python-learn/lesson5.png)

## exercise 2

Write a program which reads in a value `n` from the user and 
adds up all of the odd numbers less than or equal to `n`.  
This value should be printed out.

## exercise 3

* Create a jupyter-notebook for problems on page 27.
* Create a jupyter-notebook for problems on page 29.


