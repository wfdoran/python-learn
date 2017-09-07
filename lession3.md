# Lession 3

## loops

```python
print("Start")
for i in range(10):
    print(i)
print("End")
```

There are three important concepts in this short example.  The first is
a "block" of code.  A block of code is a set of python instructions 
and commands indented at a certain level or further.  A block ends 
at the first instruction with less indenting.  In this example, 
`print(i)` is a block of code with the `print("End")` ending the block.  

The second important concept is `range`.  The range `range(10)` will take on the 
values `{0,1,2,...,9}` one at a time.  In general `range(n)` will take on 
the values `{0,1,2,...,n-1}`.  

The third new concept which combines the previous two is the `for` loop.  This 
runs the block below it with `i` taking on each of the values in  `range(10)`.
This is done one at a time, first with `i=0`.  Then with `i=1`, `i=2`, and so on
until `i=9`.  

## examples

Sum the number from 0 to 10.  

```python
s = 0
for i in range(11):
    s = s + i
print(s)
```

Note that we needed `range(11)` in order for `10` to be included.

Draw a square.  

```python
from turtle import *
shape("turtle")
for _ in range(4):
    forward(100)
    right(90)
```

Here we only used `range(4)` to execute the code block 4 times.  We
did not use its value.   As a convention, we will use the valid variable `_` 
in such siturations to indicate the the value is not used.

Here is a nested loop. 

```python
for i in range(4):
    print(i, "<", end="")
    for j in range(5)
        print(j, end=",")
    print(">")
```       

## more on code blocks

In python, indenting is always spaces (not tabs) and always a 
multiple of 4 spaces. See [PEP8](https://www.python.org/dev/peps/pep-0008/) for the 
style rules for python.  In python whitespace matters!


## more on range

`range` is an iterator which each time it is called or accessed, returns the next value.
This means the following is gives a pretty meaningless result. 

```python
print(range(10))
```

But you can convert a range to a list, which we will talk about more later, and 
print that. 

```python
print(list(range(10))
print(list(range(18))
```

Now, let's play with more general ranges with two or three parameters. 
```python
print(list(range(3,12)))
print(list(range(-4,5)))

print(list(range(0,10,2)))
print(list(range(0,13,3)))
print(list(range(10,0,-1)))
```

## more on for loops

