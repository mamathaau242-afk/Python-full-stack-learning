# Day 7

## Key Learnings

### Inheritance
Inheritance allows us to define a class that inherits all the methods and properties from another class.
- Parent class is the class being inherited from, also called base class.
- Child class is the class that inherits from another class, also called derived class.
```python
class Animals:
    def __init__(self, name):
        self.name = name
    def eat(self):
        return f"{self.name} is eating"

class Dog(Animals):
    def bark(self):
        return f"{self.name} says woof!"
my_dog = Dog("Buddy")
print(my_dog.eat()) #function call
print(my_dog.bark())
```
```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

class Developer(Employee):
    def __init__(self, name, salary, prog_name):
        super().__init__(name, salary)
        self.prog_name = prog_name

emp1 = Developer("Mamatha", 50000, "Python")
print(emp1.name)
print(emp1.salary)
print(emp1.prog_name)
```
### Polymorphism
The word "polymorphism" means "many forms", and in programming it refers to methods/functions/operators with the same name that can be executed on many objects or classes.
```python
class creditcard:
    def process_payment(self,amount):
       print(f"charing{amount} to credtcard")
class paypal:
    def process_payment(self,amount):
        print(f"Routing{amount} to paypal")
def checkout(payment_method,amount):
    payment_method.process_payment(amount)
checkout(creditcard(), 100)
checkout(paypal(), 500)
```
### Types of Polymorphism
- compile-time (static) polymorphism
   - Compile-time polymorphism allows multiple methods with the same name but different parameters, with the appropriate method selected before execution  
- runtime (dynamic) polymorphism.
   - Runtime polymorphism means that the behavior of a method is decided while program is running, based on the object calling it.  
```python
class Animal():
    def make_sound(self):
      print("animal sound")
class cat(Animal):
    def make_sound(self):
      print("cat sound")
class dog(Animal):
    def make_sound(self):
      print("dog sound")
animal=[dog(), cat(), Animal()]
for animal in animals:
  print(animal.make_sound())
```
### Encapsulation
Encapsulation is the practice of bundling data and the methods that act on that data into a single unit class.




