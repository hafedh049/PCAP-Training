## **<span style="font-weight:bold; color:rgb(0, 176, 240)">O</span><span style="color:rgb(0, 176, 80)">O</span><span style="color:rgb(255, 0, 0)">P</span> stands for <span style="color:rgb(0, 176, 240)">O</span>bject <span style="color:rgb(0, 176, 80)">O</span>riented <span style="color:rgb(255, 0, 0)">P</span>rogramming**


Let's break down the terms "class," "instance," and "object" in Python:

### Class
- **Definition**: A class is a blueprint or template for creating objects. It defines a type of data structure that contains both data (attributes) and methods (functions) that operate on that data.
- **Example**:
  ```python
  class Dog:
      def __init__(self, name, age):
          self.name = name
          self.age = age
      
      def bark(self):
          return "Woof!"
  ```

### Instance (IN MEMORY)
- **Definition**: An instance is a specific realization of a class. It is created by calling the class as if it were a function. Each instance has its own unique set of attributes and methods based on the class blueprint.
- **Example**:
  ```python
  my_dog = Dog(name="Buddy", age=3)
  ```

### Object (IN CODE)
- **Definition**: In Python, an object is a general term for any value or instance of a class. Every instance of a class is an object. So, "object" can be used as a synonym for "instance," but it is a broader term that also includes other data types like integers, strings, lists, etc.
- **Example**:
  ```python
  print(my_dog.name)  # "Buddy"
  print(my_dog.bark())  # "Woof!"
  ```

### Summary
- **Class**: A blueprint for creating objects.
- **Instance**: A specific object created from a class.
- **Object**: A general term for any instance of a class or any value in Python, including instances of classes.

In Python, when you create an instance of a class, you are also creating an object. So, while "instance" and "object" can often be used interchangeably when talking about class instances, "object" can also refer to other data types beyond class instances.


```python
class A:
	pass
```

Here we define a class named **A** that has nothing (Neither **attributes** nor **methods**)

```python
class A:
	def __init__(self, *args, **kwargs):
		self.args = args
		self.kwargs = kwargs
		print(f"args: {self.args}",f"kwargs: {self.kwargs}",sep="\n",end="\n")

obj_a = A(1,2,3,a=5,b=6)
```

This is the output:

![[Pasted image 20240801094530.png]]

So lets break the code part by part:

```python
def __init__(self, *args, **kwargs):
	...
```

This is called **constructor** and there are **2 types** of it **explicit** one and **implicit** one
the implicit constructor is created automatically and the other one need to be created using the ______init______ . The **self** argument need to be passed as the first parameter in the constructor, the self argument is a reference of the current object so we can later use it to access the object attributes like that **self.args** and **self.kwargs**

Sure! Here are examples of common class dunder methods in Python, demonstrating their usage:

### Object Creation and Initialization

```python
class MyClass(Object):
    def __new__(cls, *args, **kwargs):
        print("Creating instance")
        return super().__new__(cls)

    def __init__(self, value):
        print(f"Initializing instance with value: {value}")
        self.value = value

	def __del__(self):
        print(f"Object is destroyed")

# Usage
obj = MyClass(10)
```

### Object Representation and String Conversion

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def __repr__(self):
        return f"MyClass({self.value!r})"

    def __str__(self):
        return f"MyClass with value {self.value}"

# Usage
obj = MyClass(10)
print(repr(obj))  # MyClass(10)
print(str(obj))   # MyClass with value 10
```

### Comparison Methods

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def __eq__(self, other):
        return self.value == other.value

    def __lt__(self, other):
        return self.value < other.value

# Usage
obj1 = MyClass(10)
obj2 = MyClass(20)
print(obj1 == obj2)  # False
print(obj1 < obj2)   # True
```

### Arithmetic Operations

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def __add__(self, other):
        return MyClass(self.value + other.value)

    def __mul__(self, other):
        return MyClass(self.value * other.value)

    def __repr__(self):
        return f"MyClass({self.value!r})"

# Usage
obj1 = MyClass(10)
obj2 = MyClass(5)
print(obj1 + obj2)  # MyClass(15)
print(obj1 * obj2)  # MyClass(50)
```

### Unary Operations

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def __neg__(self):
        return MyClass(-self.value)

    def __abs__(self):
        return MyClass(abs(self.value))

    def __repr__(self):
        return f"MyClass({self.value!r})"

# Usage
obj = MyClass(-10)
print(-obj)  # MyClass(10)
print(abs(obj))  # MyClass(10)
```

### Indexing, Slicing, and Calling

```python
class MyClass:
    def __init__(self, values):
        self.values = values

    def __getitem__(self, index):
        return self.values[index]

    def __setitem__(self, index, value):
        self.values[index] = value

    def __call__(self, x):
        return f"Called with {x}"

    def __repr__(self):
        return f"MyClass({self.values!r})"

# Usage
obj = MyClass([1, 2, 3])
print(obj[1])  # 2
obj[1] = 20
print(obj)  # MyClass([1, 20, 3])
print(obj(42))  # Called with 42
```

### Context Manager Methods

```python
class MyClass:
    def __enter__(self):
        print("Entering context")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Exiting context")

# Usage
with MyClass() as obj:
    print("Inside context")
```

These examples cover a range of dunder methods, illustrating how they can be used to control the behavior of objects in different scenarios.