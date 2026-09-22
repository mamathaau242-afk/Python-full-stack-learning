# Day 3

## Key Learnings

### Arithmetic Operators in Python

Arithmetic operators are used to perform standard mathematical calculations.

- **Addition (`+`)**
- **Subtraction (`-`)**
- **Multiplication (`*`)**
- **Division (`/`)**
  - Always returns a float
- **Floor Division (`//`)**
  - Rounds down to the nearest whole number
- **Modulus (`%`)**
  - Returns the remainder 
- **Exponentiation (`**`)**
  - Power operation

### Example Code
```python
a=10
b=5
print(a+b)
print(a-b)
print(a*b)
print(a/b)
print(a//b)
print(a%b)
print(a**b)
```

# Comparison Operators in Python

Comparison operators are used to compare values. They return either `True` or `False`.

-  == : Equal to (5 == 3 → False)
-  != : Not equal to (5 != 3 → True)
-  > : Greater than (5 > 3 → True)
-  < : Less than (5 < 3 → False)
-  >= : Greater than or equal to
-  <= : Less than or equal to

### Example Code
```python
a, b = 10,5
print(a == b)   
print(a != b)   
print(a > b)    
print(a < b)    
print(a >= b)   
print(a <= b)   
```

# Logical Operators

Used to combine conditional statements.

- and : Returns True if both statements are true (x < 5 and x < 10)
- or : Returns True if at least one statement is true (x < 5 or x < 4)
- not : Reverses the result (returns False if the result is true)

