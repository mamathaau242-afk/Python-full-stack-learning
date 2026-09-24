# Day 2 

## Key Learnings

## Python Control Flow: Logic, Loops & Syntax

### 1. Syntax & Boolean Operators
- ==(comparison) Equal to
- !=(comparison) Not equal to
- <,>(comparision) Less than/Greater than
- and(logical) Returns true if both conditions are true
- or(logical) Returns true if atleast one condition is true
- not(logical) Inverts the boolean value

### 2. Conditional Statements (if, elif, else)
Conditional statements evaluate boolean conditions from top to bottom. As soon as one condition evaluates to True, its indented block executes and the remaining clauses are skipped.
```python
# Example: Evaluating letter grades using if-elif-else score = 85
if score >= 90:
  print("Grade: A")
elif score >= 80:
  print("Grade: B")  # Executes! (85 >= 80 is True)
elif score >= 70:
  print("Grade: C")
else:
  print("Grade: F")
```
### 3. Definite Iteration (for Loops & range)
A for loop iterates over a defined sequence (list, string, tuple) or a generated numerical sequence using range(start, stop, step).
```python
# Iterating over a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
  print(fruit)

# Using range(start, stop, step) -> generates 2, 4, 6, 8, 10
for i in range(2, 11, 2):
  print(f"Even number: {i}")
```
### 4. Indefinite Iteration (while Loops)
A while loop executes repeatedly as long as its governing condition remains True. Important: Always ensure a variable state update inside the loop body to avoid infinite execution.
```python
# Countdown timer with explicit state update
count = 5
while count > 0:
  print(f"Countdown: {count}")
  count -= 1  # Crucial state update!
print("Blastoff!")
```
### 5. Advanced Control Flow & Special Clauses
- break: Immediately exits the loop, bypassing any remaining iterations. 
- continue: Skips the rest of the current iteration and jumps directly to the next loop evaluation. - Loop else clause: Executes only if the loop completes all iterations normally without hitting a break statement.
```python
# Searching for a prime number using loop-else
target = 7
for i in range(2, target):
  if target % i == 0:
    print(f"{target} is not prime")
    break
else:
  print(f"{target} is a Prime Number!")  # Executes because break was never triggered
```




