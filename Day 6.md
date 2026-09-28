# Day 6

## Key Learnings

### Function
- A function is a block of code which only runs when it is called.
- A function can return data as a result.
- A function helps avoiding code repetition.

### Function Fundamentals
- the def keyword
- parameters
- return values

### Creating a Function
In Python, a function is defined using the def keyword, followed by a function name and parentheses
```python
def my_function():
  print("Hello from a function")
```
### Calling a Function
To call a function, write its name followed by parentheses
```python
def my_function():
  print("Hello from a function")
my_function()
```
### Local variable
A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.
```python
def myfunc():
  x = 300
  print(x)
myfunc()
```
### Nonlocal Keyword
- The nonlocal keyword is used to work with variables inside nested functions.
- The nonlocal keyword makes the variable belong to the outer function.
```python
def myfunc1():
  x = "Jane"
  def myfunc2():
    nonlocal x
    x = "hello"
  myfunc2()
  return x
print(myfunc1())
```
### Global Scope
- A variable created in the main body of the Python code is a global variable and belongs to the global scope.
- Global variables are available from within any scope, global and local.
```python
x = 300
def myfunc():
  print(x)
myfunc()
print(x)
```
### Global Keyword
- If you need to create a global variable, but are stuck in the local scope, you can use the global keyword.
- The global keyword makes the variable global.

Example
If you use the global keyword, the variable belongs to the global scope:
```python
def myfunc():
  global x
  x = 300
myfunc()
print(x)
```
