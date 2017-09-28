# Lesson 5

## Boolean Variables

```python
x = 5 > 3
y = 5 > 8
z = 5 == 5
print(x,y,z)
print(type(x))
```

A boolean variable takes on the value `True` or `False` and 
indicates whether an expression is correct.  The basic 
comparision operations are given the following table. 

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

All of comparisons we have done involve integers.  Things can get 
more complicated with other variable types.  

```python
print(0.33333333333333333333333 == 1/3)
print(0.33333333 == 1/3)
```

What happend here?  The persion of the floating piont number
matters.  As general rule, you should not compare floats for 
equality.  You can use less than and greater than without 
worry, but equality is tricky.  

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

```python
print("abc" > "aaa")
print("aaaa" > "aaa")
print("zzz" > "aaa")
print("ZZZ" > "aaa")
```
## if-then-else

```python
evens = 0
odds = 0
for i in range(10):
    if i % 2 == 0:
       evens = evens + i
    else:
       odds = odds + i
print(evens, odds)
```

## and, or, not

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

```python
total = 0
for i in range(100):
    if (i % 2 == 0) and (i % 7 == 0) and (not (i % 14) == 0):
       total += i
print(total)
```

## exercise 1 

Create square spiral

## exercise 2

## exercise 3



