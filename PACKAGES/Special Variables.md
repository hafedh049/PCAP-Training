### Common Special Variables

1. **`__name__`**:
    
    - Represents the name of the current module.
    - If the module is being run as the main program, its value is `'__main__'`.
 
 ```python
if __name__ == '__main__':     
	print("This script is being run directly") 
else:     
	print("This script is being imported")
```
    
2. **`__doc__`**:
    
    - Contains the documentation string for a module, class, method, or function.

```python
def example():
	"""This is a docstring for the example function."""
	pass
	
print(example.__doc__)
```
    
3. **`__file__`**:
    
    - Represents the pathname of the file from which the module was loaded.
 
```python
print(__file__)
```
    
4. **`__package__`**:
    
    - Indicates the package name for the module.

```python
print(__package__)
```
    
5. **`__version__`**: **(CREATED)**
    
    - A convention for indicating the version of a module or package.

```python
__version__ = "1.0.0" 
print(__version__)
```

### Special Variables in Classes

1. **`__init__`**:
    
    - A constructor method for initializing an instance of a class.

```python
class MyClass:
	def __init__(self, value):
		self.value = value
```
    
2. **`__del__`**:
    
    - A destructor method that is called when an object is about to be destroyed.

```python
class MyClass:
    def __del__(self):
		print("Object is being destroyed")
```
    
3. **`__repr__`**:
    
    - A method that returns an **"Official"** string representation of an object.

```python
class MyClass:
	def __init__(self,value):
		self.value = value
	def __repr__(self):
		return f"MyClass(value={self.value})"

c = MyClass(5)
l = [c,c]
print(repr(c))
print(l)
#[MyClass(value=5), MyClass(value=5)]
```
    
4. **`__str__`**:
    
    - A method that returns a **"Nice"** string representation of an object.

```python
class MyClass:
	def __str__(self):
	    return f"MyClass with value {self.value}"
c = MyClass()
print(c)
"or"
print(str(c))
```
    
5. **`__dict__`**:
    
    - A dictionary or other mapping object used to store an object's **(writable)** attributes.

```python
obj = MyClass(10) 
print(obj.__dict__)
```
    
6. **`__class__`**:
    
    - The class to which an instance belongs.

```python
print(obj.__class__)
```

### Special Variables in Functions

1. **`__annotations__`**:
    
    - A dictionary containing variable annotations including the return type.

```python
def example(a: int, b: str) -> float:
    return float(a)
    
print(example.__annotations__)
```
    
2. **`__defaults__`**:
    
    - A tuple containing default argument values for the positional and keyword parameters.

```python
def example(a, b=2):     
	return a + b  

print(example.__defaults__)
```

### Other Special Variables

1. **`__builtins__`**:
    
    - A reference to the built-in module named `builtins`.

```python
print(__builtins__.len("555"))
```
    
2. **`__import__`**:
    
    - A function that is invoked by the `import` statement.

```python
module = __import__('math')
print(module.sqrt(16))
```