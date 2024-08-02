In Python, private, public, and final attributes and methods are implemented differently than in some other languages. Python follows a naming convention approach rather than strict enforcement. Here’s how each type is generally used:

### Public Attributes and Methods

By default, all attributes and methods in Python are public. This means they can be accessed from outside the class.

```python
class MyClass:
    def __init__(self, value):
        self.public_value = value  # Public attribute

    def public_method(self):
        return f"Public method called with value {self.public_value}"

# Usage
obj = MyClass(10)
print(obj.public_method())  # Public method called with value 10
print(obj.public_value)     # 10
```

### Private Attributes and Methods

Private attributes and methods are intended to be accessed only within the class. They are defined with a leading underscore (`_`) or double underscore (`__`). 

- **Single Underscore (_)**: A single underscore suggests that an attribute or method is intended to be private but can still be accessed from outside the class if necessary.

- **Double Underscore (__)**: A double underscore triggers name mangling, which makes the attribute or method harder to access from outside the class.

#### Single Underscore Example

```python
class MyClass:
    def __init__(self, value):
        self._protected_value = value  # Protected attribute

    def _protected_method(self):
        return f"Protected method called with value {self._protected_value}"

# Usage
obj = MyClass(10)
print(obj._protected_method())  # Protected method called with value 10
print(obj._protected_value)     # 10
```

#### Double Underscore Example

```python
class MyClass:
    def __init__(self, value):
        self.__private_value = value  # Private attribute

    def __private_method(self):
        return f"Private method called with value {self.__private_value}"

# Usage
obj = MyClass(10)
# The following lines will raise an AttributeError
# print(obj.__private_method())
# print(obj.__private_value)

# Accessing private attributes through name mangling
print(obj._MyClass__private_method())  # Private method called with value 10
print(obj._MyClass__private_value)     # 10
```

### Final Attributes and Methods

Python does not have built-in support for final attributes and methods like some other languages (e.g., Java). However, you can use conventions and techniques to achieve similar behavior.

#### Convention for Final Attributes and Methods

1. **Use Comments**: Document that a method or attribute should not be overridden or changed.

2. **Using a Metaclass**: Create a metaclass that prevents overriding of methods.

3. **Using `@final` Decorator** (Python 3.8+): The `typing` module provides a `@final` decorator to indicate that a method should not be overridden.

##### Example of `@final` Decorator

```python
from typing import final

class Base:
    @final
    def final_method(self):
        return "This method cannot be overridden"

class Derived(Base):
    # Uncommenting the following line will cause a type checker warning
    # def final_method(self):  # Error: Cannot override final method
    #     return "Attempt to override"

# Usage
obj = Base()
print(obj.final_method())  # This method cannot be overridden
```

In summary:
- **Public** attributes and methods are accessible from anywhere.
- **Protected** (single underscore) attributes and methods are intended to be internal but are still accessible from outside.
- **Private** (double underscore) attributes and methods are harder to access from outside due to name mangling.
- **Final** methods and attributes can be indicated using conventions or the `@final` decorator but are not strictly enforced by the language.

In Python, there isn’t a built-in concept of a “final” attribute that you can enforce at the language level, unlike some other languages such as Java. However, you can use conventions and certain techniques to achieve similar behavior.

### Convention for Final Attributes

1. **Naming Convention**: Use naming conventions to indicate that an attribute should not be modified after initialization. For instance, use an uppercase name for attributes that are intended to be final.

2. **Document Intent**: Clearly document in the class docstring or comments that certain attributes are intended to be immutable.

### Example Using Naming Convention

```python
class MyClass:
    def __init__(self, value):
        self.FINAL_VALUE = value  # Final attribute by convention

    def get_final_value(self):
        return self.FINAL_VALUE

# Usage
obj = MyClass(10)
print(obj.get_final_value())  # 10

# Modifying the attribute directly (not recommended, but possible)
obj.FINAL_VALUE = 20
print(obj.get_final_value())  # 20
```

### Using Property Decorators to Enforce Immutability

You can use Python’s `property` decorator to create a read-only attribute that acts like a final attribute.

```python
class MyClass:
    def __init__(self, value):
        self._value = value  # Private attribute

    @property
    def value(self):
        return self._value

    # No setter defined, making 'value' effectively final
    # Attempting to set this will raise an AttributeError
    # @value.setter
    # def value(self, new_value):
    #     raise AttributeError("Cannot modify final attribute")

# Usage
obj = MyClass(10)
print(obj.value)  # 10

# Attempting to modify will raise an error
# obj.value = 20  # Uncommenting this line will raise AttributeError
```

### Using `@dataclass` with `frozen=True`

If you’re using the `dataclasses` module in Python, setting `frozen=True` will make instances of the class immutable, meaning all attributes are effectively final.

```python
from dataclasses import dataclass

@dataclass(frozen=True)
class MyClass:
    value: int

# Usage
obj = MyClass(10)
print(obj.value)  # 10

# Attempting to modify will raise an error
# obj.value = 20  # Uncommenting this line will raise AttributeError
```

### Using a Metaclass (Advanced)

You can use a metaclass to enforce that certain attributes are not modified. This is a more advanced technique and usually overkill for most use cases.

```python
class FinalMeta(type):
    def __setattr__(cls, name, value):
        if name in cls.__dict__:
            raise AttributeError(f"Cannot modify final attribute {name}")
        super().__setattr__(name, value)

class MyClass(metaclass=FinalMeta):
    FINAL_VALUE = 10

# Usage
obj = MyClass()
print(obj.FINAL_VALUE)  # 10

# Attempting to modify will raise an error
# MyClass.FINAL_VALUE = 20  # Uncommenting this line will raise AttributeError
```

In summary:
- **Naming Conventions** and **documentation** can suggest that attributes should not be modified.
- **Property decorators** can create read-only attributes.
- **Dataclasses** with `frozen=True` make all attributes immutable.
- **Metaclasses** can enforce immutability in more complex scenarios.