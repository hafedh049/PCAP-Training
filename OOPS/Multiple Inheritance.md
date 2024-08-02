Multiple inheritance in Python allows a class to inherit from more than one parent class. This can be useful but also complex, especially when dealing with method resolution order (MRO) and calling multiple superclass methods. Here’s a breakdown of how to work with multiple inheritance and call methods from multiple superclasses.

### Basic Multiple Inheritance

Here’s an example of multiple inheritance where a class inherits from two parent classes:

```python
class ParentA:
    def method_a(self):
        return "Method from ParentA"

class ParentB:
    def method_b(self):
        return "Method from ParentB"

class Child(ParentA, ParentB):
    def method_child(self):
        return "Method from Child"

# Usage
obj = Child()
print(obj.method_a())  # Method from ParentA
print(obj.method_b())  # Method from ParentB
print(obj.method_child())  # Method from Child
```

### Method Resolution Order (MRO)

Python uses the C3 linearization algorithm to determine the method resolution order (MRO). You can view the MRO of a class using the `__mro__` attribute or the `mro()` method.

```python
class ParentA:
    def method(self):
        return "Method from ParentA"

class ParentB:
    def method(self):
        return "Method from ParentB"

class Child(ParentA, ParentB):
    pass

# Check MRO
print(Child.__mro__)  # (<class '__main__.Child'>, <class '__main__.ParentA'>, <class '__main__.ParentB'>, <class 'object'>)
print(Child.mro())   # [<class '__main__.Child'>, <class '__main__.ParentA'>, <class '__main__.ParentB'>, <class 'object'>]
```

### Calling Multiple Superclasses’ Methods

To explicitly call methods from multiple superclasses, you can use the `super()` function. However, with multiple inheritance, this can become complex. Here’s how you might handle it:

```python
class ParentA:
    def method(self):
        print("Method from ParentA")

class ParentB:
    def method(self):
        print("Method from ParentB")

class Child(ParentA, ParentB):
    def method(self):
        super().method()  # Calls method from ParentA based on MRO
        print("Method from Child")

# Usage
obj = Child()
obj.method()  
# Output:
# Method from ParentA
# Method from Child
```

In this example, `super().method()` calls `method` from `ParentA` because `ParentA` appears before `ParentB` in the MRO.

### Customizing Method Resolution Order

If you need to customize the method resolution order or explicitly call methods from specific superclasses, you can directly call them by specifying the parent class.

```python
class ParentA:
    def method(self):
        print("Method from ParentA")

class ParentB:
    def method(self):
        print("Method from ParentB")

class Child(ParentA, ParentB):
    def method(self):
        ParentA.method(self)  # Explicitly call method from ParentA
        ParentB.method(self)  # Explicitly call method from ParentB
        print("Method from Child")

# Usage
obj = Child()
obj.method()  
# Output:
# Method from ParentA
# Method from ParentB
# Method from Child
```

### Example with Initialization

Here's an example where each parent class has an `__init__` method, and you need to ensure that each `__init__` method is called properly:

```python
class ParentA:
    def __init__(self, a):
        self.a = a
        print(f"Initialized ParentA with {a}")

class ParentB:
    def __init__(self, b):
        self.b = b
        print(f"Initialized ParentB with {b}")

class Child(ParentA, ParentB):
    def __init__(self, a, b):
        ParentA.__init__(self, a)
        ParentB.__init__(self, b)
        print(f"Initialized Child with {a} and {b}")

# Usage
obj = Child(1, 2)
# Output:
# Initialized ParentA with 1
# Initialized ParentB with 2
# Initialized Child with 1 and 2
```

### Summary

- **Basic Multiple Inheritance**: Python supports multiple inheritance, where a class can inherit from multiple parent classes.
- **MRO (Method Resolution Order)**: Python determines the order in which base classes are looked up using the C3 linearization algorithm. You can view it with `__mro__` or `mro()`.
- **Calling Multiple Superclasses’ Methods**: Use `super()` to call methods according to MRO or call methods directly from specific parent classes if needed.
- **Customizing Initialization**: Explicitly call parent class initializers to ensure proper initialization in multiple inheritance scenarios.


