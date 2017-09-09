# Lession 3

## for loops

```python
print("Start")
for i in range(10):
    print(i)
print("End")
```

There are three important concepts in this short example.  The first
is a "block" of code.  A block of code is a set of python instructions
and commands which will be executed as a unit.  Python uses indention 
(how far to the right a line starts) to signify a block.  A block starts 
with a line indented further than the line
above and continues so long as you stay at this or further level of indenting.
In this example, `print(i)` is a block of code as it is indented.  

The second important concept is `range`.  `range(10)` will take on the 
values `{0,1,2,...,9}` one at a time.  In general `range(n)` will take on 
the values `{0,1,2,...,n-1}`.  

The third new concept which combines the previous two is the `for` loop.  This 
runs the block below it with `i` taking on each of the values in  `range(10)`.
This is done one at a time, first with `i=0`.  Then with `i=1`, `i=2`, and so on
until `i=9`.  

## more for loop examples

Sum the number from 0 to 10.  

```python
s = 0
for i in range(11):
    s = s + i
print(s)
```

Note that we need `range(11)` in order for `10` to be included.

Draw a square.  

```python
from turtle import *
shape("turtle")
for _ in range(4):
    forward(100)
    right(90)
```

Here we only used `range(4)` to execute the code block 4 times.  We
did not use its value.  As a convention, we will use the valid but
silly variable `_` in such situations to indicate the the value is
not used.

Here is a nested loop with nested code blocks.

```python
for i in range(4):
    print(i, "<", end="")
    for j in range(5):
        print(j, end=",")
    print(">")
```       

There are using some advanced features of `print` in this example.
Normally, print ends by printing a new line and further printing
starts on the next line.  By setting print's `end` variable, you can
change how print finishes.  With `end=""`, print finishes with nothing
and further printing will occur on the same line.  With `end=","`, it
will print a comma and continue further printing on the same line.

## more on code blocks

In python, indenting is always spaces (not tabs) and always a multiple
of 4 spaces. See [PEP8](https://www.python.org/dev/peps/pep-0008/) for
the style rules for python.  In python whitespace matters!

## more on range

`range` is an iterator which each time it is called or accessed,
returns the next value.  This means the following is gives a pretty
meaningless result.

```python
print(range(10))
```

But you can convert a range to a list, which we will talk about more
later, and print that.

```python
print(list(range(10)))
print(list(range(18)))
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

The syntax is

```python
for <variable> in <iterator>:
    <code_block>
```

`range(n)` is just one iterator, we will learn about many more
as we go.  `for`, `in`, and the final colon have to be just 
like that.  You cannot change these.  This is how you tell python
you want a for loop. 

One final example

```python
for i in range(3):
    print(i)
print("Done with i = ", i)
```

The value `i` persists outside of the for loop with the last 
value it took.  

## Exercise 1

Write a program which 
* Asks the user for a positive integer n.
* Computes and prints `sum = 1 + 2 + ... + n`.
* Computes and prints `sum_squares = 1*1 + 2*2 + ... + n*n`.
* Computes and prints `sum_cubes = 1*1*1 + 2*2*2 + ... + n*n*n`.
* Finally it print out `sum * sum`. 

## Exercise 2

Write a program which 
* Asks the user for an integer n >= 3.
* Using turtle graphics, draws an n-gon with side length 100.

## Exercise 3

* Create a jupyter-notebook for problems on page 19.
* Create a jupyter-notebook for problems on page 21.

