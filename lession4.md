# Lession 4

## Lists

A list in python is an ordered array of variables.

```python
x = [0,1,4,9,16]
print(x)
print(x[0])
print(x[3])
print(x[-1])
pirnt(x[7])
```

The syntax for a list  (`[ , , ]`) uses square braces to denote the 
start and end of the list.  The entries in the list are separated by 
commas.  In the above example, the variable `x` contains the entire 
list.  Individual entries in a list can be obtained by their index, 
`x[index]`.  Python is a 0-index language which means that `x[0]` is 
the first entry in the list.  Negative values give entries from the 
end.  So, `x[-1]` is the last entry.  Since `x` contains 5 entries, 
`x[4]` is also the last entry. 

## List type

```python
x = [1, "hello", 7.3]
print(x)
print(x[1])
type(x)
type(x[0])
type(x[1])
type(x[2])
```

A list may contain variables of different types.  

## Initializing lists

Last week, we learned about the `list(s)` function.  It tries to 
convert `s` into a list if it can. 

```python
x = list(range(5))
print(x)
```

Here `range(5)` is not a list itself; it is an iterator.  But `list()`
can convert it into a list.

```python
n = 5
x = [0] * n
print(x)
for i in range(n):
    x[i] = i * i
print(x)
```

Two things here.  First, `[0] * n` creats a list of n 0's.  Second,
not only can you read individual elements of `x`, you can set them 
with `x[i] = value`.

```python
x = []
for i in range(5):
    print(x)
    x.append(i * i)
print(x)
```

Here we start with "empty" list.  Yes that is allowed, but don't try
print any `x[i]`.  Then we use the `append` method to add values to 
the end of `x`.

## Operations

Operations read in a list and produce some value, but do not change the
list.  Here are few.

```python
x = [1,3,2,6,1]
print(len(x))
print(sum(x))
```

The syntax for an operations is `value = operation( list_var )`.  

## Methods  

Method alter the list.  We have already seen `x.append()`.  Here are two
more.

```python
x = [1,3,2,6,1]
x.sort()
print(x)
x.reverse()
print(x)
```

The syntax for a method is `list_var.method(args)`.  `list_var` is 
usually altered and there is often no return value.  
Later we will learn many more operations and methods.


## Exercise 1

## Exercise 2

## Exercise 3



