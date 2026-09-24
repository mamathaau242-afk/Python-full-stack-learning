# Day 5

## key learnings

### 1.Python strings
- Immutable ordered sequences enclosed in single or double quotes.
- original strings elements cannot be changed or assigned in place after creation.
- slicing syntax: [start:stop:step]

### String Method & Formatting
- .strip() & .split() : Removes leading spaces and divides string into a list based on delimiters.
- .join() : Combines iterable list items into a single string connected by specified character.
- f-strings : Evaluates embedded python expressions directly inside string literals seamlessly.
```python
data= "data,science,ai"
cleaned=data.strip()
topics=cleaned.split(",")
formatted="->".join(topics)
status="Active" summary= f"Pipeline:{formatted} | status: {status}"
print(summary)
```
### 2.Nested Dictionary Operations
- key chaining
    - use sequential brackets [k1][k2] to navigate deep levels of hierarchy.
- Safe Lookup
    - chain .get() calls to avoid keyError exceptions when key might be missing.
- In-Place Edits
    - Directly assign to dict[k1][k2]=new_val to update specific nested properties.
```python
students={"s101":{"name":"Alice", "major":"cs", "gpa":3.9}, "s102":{"name":"bob", "major":"cs", "gpa":3.5}}
students["s101"]["gpa"]
students["s102"]["gpa"]=3.7 #Add new key to inner dictionary
students["s101"]["status"]="Graduated"
```
### Nested IF Execution Logic
- level 1: Outer IF
    - checks age>=18. if false, immediately short-circuits to underage exit.
- level 2: Sub-IF
    - Evaluates has_ticket only after age check evaluates to true.
- level 3: Deep-IF
    - Differentiates between VIP and standard zones based on is_vip flag.

### Nested FOR Loop Patterns
- outer loop(i)
    - controls major row movements. Increments only after the inner loop finishes.
- Inner Loop(j)
    - Processes horizontal columns completely for every single step of i.
- Time complexity
    - Yields 0(N *M) performance. Avoid 3+deep nesting in large datasets.
```python
for i in range(1,4):
  for j in range91,4):
  product=i*j
  print(f"{i}*{j}={product}",end="\t")
print()
```
### Nested WHILE Loops
- Counter Reset Rule
    - col=1 must occur Ensure both col+=1 and row+=1 progress toward terminate conditions.


    


  

  
