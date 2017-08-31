# Lession 2

## variables

Variables are human understandable names for things.  So far, the only 
thing we know about are strings. 

```python
x = "hello"
```

`x` is the variable name and `"hello"` is the variable value.  Variables
get their value by an assignement statement like the one above with an equal
sign `=` signifying the assignment. 

You can reassign variables

```python
x = "hello"
print(x)
x = "world"
print(x)
```

Case matters.  In the following `x` and `X` are different variable names.

```python
x = "hello"
X = "world"
print(x,X)
```

What names are allowed?  
* The first character must be a letter `a-zA-Z` or underscore `_`.
* After the first character, numbers `0-9` are allowed. 
* Spaces and special characters such as `!@#$%^&*()-+=[]{}|\/?,.` are not 
  allowed in variable names.
* Certain special names are reserved by python.  We will learn these 
  as we go.  Editors often know these words and color them differently.
  Try `def = 5` for example.

The *type* of a variable is sort of stuff stored in that variable. 
You can always ask python what that is.

```python
x = "hello"
type(x)
```

## Integers

Another type of variable is integers `{...,-2,-1,0,1,2,...}`.  
You can do all kinds of math with integers. 

```python
a = 5           # assign variable a to hold the interger value 5 
type(a)
b = 3           # assign b to 3
a + b           # add
a - b           # substract
a * b           # multiply
a // b          # integer division
a % b           # remainder after division
a ** b          # expoentation
```

## Conversion

Try

```python
a = "5"
b = "3"
print(a+b)
```

Hmmm.... `a` and `b` are strings and `+` for strings is concatenation.
If you want to add 5 and 3 as integers, you need to first convert the
strings a and b to integers.

```python
a = "5"
b = "3"
aa = int(a)
bb = int(b)
print(aa + bb)
```

## Exercise 1

Which of the following is a valid python variable name?
1 What'sUp
2 HowAreYouDoing
3 HavingFun?
4 _first_timer
5 string_number1
6 STRONG     
7 def
8 DEF
9 4daddy

## Exercise 2

Fix the bugs in the following program 



## Exercise 3

Write a program which
* Asks the user for two integers.
* Print out the sum, difference, product, and division of these two integers.

```python
a = input("Enter an integer? ")
b = input("Enter another integer? ")
print(a,b)
```

## Exercise 4

By experimenting, work out what python does when you multiply a string
by an integer.

```python
"hello" * 5
```
