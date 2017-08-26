# Lession 1

## Hello World (Four Ways)

* interactive 

```
> python

>>> print("Hello World!")
```

* idle

```
> idle

>>> print("Hello World!")
```

* run a python program

Create the file `prog1.py`
```
print("Hello World!")
```

Run
```
> python prog1.py
```

* jupyter notebook

Run "Jupyter Notebook" from start menu and wait for browser to start.   
In upper-right, click `new` and select `Python 3`.  In the first cell,
type in `print("Hello World!` and then Ctrl-Enter to run the command.


## New Python Commands

```python
print()                   # prints something
s = "string"              # string variable
s.upper()                 # converts to uppercase
t = "Hello " + "World"    # concatenates strings
x = input("What? ")       # reads input from user
```

## Turtle Graphics Intro

```python
from turtle import *
shape("turtle")
forward(100)
left(90)
forward(50)
right(90)
forward(200)
reset()
quit()
```

## Exercise 1

Fix this program

```python
s = "Hello "
t = "World!'
r = t.upper
print s t
```

## Exercise 2

Write a program which
* Asks the user "What is your name?"
* Reads in the name.
* Converts the nume to uppercase.
* Print "Hello " and the uppercased name.

## Exercise 3

Turtle graphics exercises on page 13.



