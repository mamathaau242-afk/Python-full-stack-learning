# Day 2 

## Key Learnings

### List Methods
- **append()** → Adds values at the end  
- **insert()** → Adds values at a specified position  
- **clear()** → Removes all values from the list  
- **del()** → Deletes the list  
- **copy()** → Returns a copy of the list  
- **count()** → Returns the number of elements with the specified value  
- **extend()** → Adds elements from another list  
- **index()** → Returns the position of the first occurrence  
- **pop()** → Removes the last element (or a specified position)  
- **remove()** → Removes the first occurrence of a value  
- **reverse()** → Reverses the list order  
- **sort()** → Sorts the list in ascending/descending order
```python
a=[1,2,3,4,5]
a.append(6)
print(a)      #output [1, 2, 3, 4, 5, 6]

a.insert(0,0)
print(a)           #output [0, 1, 2, 3, 4, 5, 6]

a=[1,2,3,4]                                                
print(a.count(1))  #output 1

a.pop()
print(a)  #output [1, 2, 3]

a.extend([5,6])
print(a)          #output [1, 2, 3, 5, 6]

a.remove(2)
print(a)     #output [1, 3, 5, 6]

a = [1, 2, 3, 4, 5]
print(a.index(4))   #output 3

a.reverse()
print(a)      #output [5, 4, 3, 2, 1]

a.sort()
print(a)   #output [1, 2, 3, 4, 5]
```
### Tuple Methods
- **count()** → Returns number of times a value appears  
- **index()** → Returns position of first occurrence
  
### Dictionary Methods
- **clear()** → Removes all items from the dictionary  
- **copy()** → Returns a shallow copy of the dictionary  
- **get()** → Returns the value of the specified key  
  - Example: `course.get("duration", "unknown")` → returns `"unknown"` if `"duration"` key is not present  
- **pop()** → Removes item with specified key  
- **popitem()** → Removes the last inserted key-value pair  
- **fromkeys()** → Creates a dictionary from given keys  
- **items()** → Returns a list of key-value pairs (tuples)  
- **keys()** → Returns a list of dictionary keys  
- **values()** → Returns a list of dictionary values  
- **setdefault()** → Returns the value of a key; sets default if not present
```python
course = {"name": "Python", "level": "Beginner", "duration": "3 months"}

course.clear()
print(course)        #output {}

course = {"name": "Python", "level": "Beginner"}
copy_course = course.copy()
print(copy_course)      #output {'name': 'Python', 'level': 'Beginner'}

print(course.get("duration", "unknown"))   #output unknown

print(course.pop("level"))
print(course)   #output Beginner

print(course.popitem())
print(course)  #output {'name': 'Python'}

student = {"id": 101, "name": "Mamatha"}
print(list(student.items()))   #output [('id', 101), ('name', 'Mamatha')]

print(list(student.keys()))    #output ['id', 'name']

print(list(student.values()))  #output [101, 'Mamatha']

print(student.setdefault("age", 22))
print(student)    #output {'id': 101, 'name': 'Mamatha', 'age': 22}
```

### Set Methods
- **add()**, **clear()**, **copy()**  
- **difference()**, **difference_update()**  
- **discard()**, **pop()**, **remove()**  
- **union()**, **update()**  
- **intersection()**, **intersection_update()**  
- **symmetric_difference()**  
- **issubset()**, **issuperset()**, **isdisjoint()**
```python
a={1,2,3,4}
a.add(5)
print(a)   #output {1, 2, 3, 4, 5}

a.clear()
print(a)   #output set()

a={1,2,3,4}
b=a.copy()
print(b)    #output {1, 2, 3, 4}

a.discard(0)
print(a)      #output {1, 2, 3, 4}

a.discard(3)
print(a)      #output {1, 2, 4}

a.pop()
print(a)    #output {2, 4}

a.remove(4)
print(a)       #output {2}

a={1,2}
b={2,3,4}
print(a.union(b))   #output {1, 2, 3, 4}

a={1,2,3}
b={2,3,4}
print(a.difference(b))  #output {1}

a={1,2,3}
b={2,3,4}
print(b.difference(a))  #output {4}

a={1,2,3}
b={2,3,4}
print(a.difference_update(b))    #output None
print(a,b)                       #output {1} {2, 3, 4}

a={1,2,3}
b={2,3,4}
print(b.difference_update(a))    #output None
print(a,b)                       #output {1, 2, 3} {4}
```



