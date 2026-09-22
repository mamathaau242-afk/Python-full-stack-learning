# Day 3

## Key Learnings

## Operators in Python

### Arithmetic Operators

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
print(a+b)  #output 15
print(a-b)  #output 5 
print(a*b)  #output 50
print(a/b)  #output 2.0
print(a//b) #output 2
print(a%b)  #output 0
print(a**b) #output 100000
```

# Comparison Operators 

Comparison operators are used to compare values. They return either `True` or `False`.

- **Equal (`==`)**
- **Not Equal (`!=`)**
- **Greater Than (`>`)**
- **Less Than (`<`)**
- **Greater Than or Equal (`>=`)**
- **Less Than or Equal (`<=`)**
  
### Example Code
```python
a, b = 10,5
print(a == b)   #output False
print(a != b)   #output True
print(a > b)    #output True
print(a < b)    #output False
print(a >= b)   #output True
print(a <= b)   #output False
```

# Logical Operators

Used to combine conditional statements.

- **and** : Returns True if both statements are true (x < 5 and x < 10)
- **or** : Returns True if at least one statement is true (x < 5 or x < 4)
- **not** : Reverses the result (returns False if the result is true)

## Example code
```python
print(a>b and a<b)
print(a>b or a<b)
print(a>b)
```

# Bitwise Operators 

Bitwise operators work directly on the binary representation of numbers.

- **AND (`&`)**
- **OR (`|`)**
- **XOR (`^`)**
- **NOT (`~`)**
- **Left Shift (`<<`)**
  - Shifts bits to the left, filling with zeros
- **Right Shift (`>>`)**
  - Shifts bits to the right, discarding bits

### Example Code
```python
x=2
print(f"{x:04b}")
print(f"{(x << 1):04b}")
print(f"{(x >> 1):04b}")

x=15
print(f"{x:08b}")
print(f"{(x << 1):08b}")
print(f"{(x >> 1):08b}")
```

# Assignment Operators 

Assignment operators are used to assign values to variables and update them.

- **`=` (Assign)**
  - Assigns the value on the right to the variable on the left
- **`+=` (Add and Assign)**
  - Adds the right operand to the left operand and assigns the result
- **`-=` (Subtract and Assign)**
  - Subtracts the right operand from the left operand and assigns the result
- **`*=` (Multiply and Assign)**
  - Multiplies the left operand by the right operand and assigns the result
- **`/= `(Division and Assignment)**
  - Divides the left operand by the right operand and assigns the result

### Example Code
```python
a=10
b=a
print(a)
print(b)
b += a
print(b)
b -= a
print(b)
b *= a
print(b)
```

# Identity Operators 

Identity operators are used to compare whether two variables refer to the **same object in memory**.

- **`is`**
  - Returns `True` if both variables point to the same object
- **`is not`**
  - Returns `True` if both variables do **not** point to the same object

### Example Code
```python
a=[1,2,3,4]
b=[1,2,3,4,]
c=a
print(a is b)
print(c is a)

a=[1,2,3,4]
b=[1,2,3,4,]
c=a
print(a is not b)
print(c is not a)
```

# Membership Operators 

Membership operators are used to check whether a value is present in a sequence (like lists, strings, tuples, etc.).

- **`in`**
  - Returns `True` if the value is found in the sequence
- **`not in`**
  - Returns `True` if the value is **not** found in the sequence
  
### Example Code
```python
a=[1,2,3,4]
print(1 in a)
print(5 not in a)

a="python is a programming language"
print("python" in a )
print("language" not in a)
```

## int32 vs int64
- **int32** → 32‑bit integer 
- **int64** → 64‑bit integer 
- These are **data type sizes**
   
