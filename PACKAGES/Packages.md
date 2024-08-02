1. **Package**:
    
    - A package is a collection of modules or libraries bundled together for distribution and reuse.
    - In Python, for example, a package is a directory containing a special `__init__.py` file and multiple module files.
    
1. **Project**:
    
    - A project refers to the entire process and all the components involved in developing a software application or system.
    - It includes source code, configuration files, resources, and documentation.
    
1. **Module**:
    
    - A module is a single unit of software or a file containing Python code, Java classes, or any other language-specific code that can be imported and used by other code.
    - In Python, a module is a `.py` file that defines functions, classes, and variables.
    
1. **Library**:
    
    - A library is a collection of pre-written code that developers can use to optimize tasks and avoid reinventing the wheel.
    - It typically provides specific functionalities such as handling dates, performing mathematical operations, or managing network protocols.

1. **API (Application Programming Interface)**:
    
    - An API is a set of rules and tools that allows different software applications to communicate with each other.
    - It defines the methods and data structures that developers can use to interact with an external system or library.
    
1. **Framework**:
    
    - A framework is a comprehensive platform or structure that provides a foundation for developing software applications.
    - It includes libraries, tools, and best practices for building and deploying applications.
    - Frameworks offer a higher level of abstraction and often dictate the architecture and flow of the application. Examples include Angular for web development, Spring Boot for Java applications, and Flask for Python web applications.

### Key Differences:

- **Scope**:
    
    - **Package**: Groups related modules.
    - **Project**: Encompasses all components of a software application.
    - **Module**: Single unit of software code.
    - **Library**: Collection of reusable code for specific functions.
    - **API**: Interface for interacting with software components.
    - **Framework**: Complete platform for application development.
    
- **Usage**:
    
    - **Package**: Organizes code for distribution.
    - **Project**: Represents the entire development effort.
    - **Module**: Encapsulates specific functionalities.
    - **Library**: Provides reusable tools and functions.
    - **API**: Facilitates communication between different systems.
    - **Framework**: Guides the overall structure and development process.


![[Pasted image 20240801213259.png]]

### 1. Basic Import

Import an entire module.

```python
import math 
print(math.sqrt(16))
# Output: 4.0
```

### 2. Import with Alias

Import a module and give it a shorter alias.

```python
import numpy as np 
array = np.array([1, 2, 3])
print(array)
# Output: [1 2 3]
```

### 3. Import Specific Functions or Classes

Import specific functions or classes from a module.

```python
from math import sqrt, pi 
print(sqrt(16))  
# Output: 4.0 
print(pi)
# Output: 3.141592653589793
```
### 4. Import All Names

Import all public names from a module. **Note**: This is generally discouraged as it can lead to a cluttered namespace and potential name conflicts.

```python
from math import *
print(sqrt(16))
# Output: 4.0 
print(pi) 
# Output: 3.141592653589793
```

### 5. Import from a Package

Import a module from a package.

```python
from os import path 
print(path.exists("file.txt"))  
# Check if 'file.txt' exists
```

### 6. Relative Imports

Import modules using relative paths within a package.

- **Single Dot (`.`)**: Current package
- **Double Dot (`..`)**: Parent package

```python
# Inside a package's module
from . import sibling_module  
# Import sibling module in the same package 
from ..parent_module import ParentClass  
# Import from parent package
```

### 7. Conditional Imports

Import modules conditionally within code blocks.

```python
if some_condition:
	import module_a 
else:
	import module_b
```

### 8. Import with Custom Handling

Use `importlib` for dynamic imports.

```python
import importlib 
module_name = 'math' 
math = importlib.import_module(module_name)
print(math.sqrt(16))
# Output: 4.0
```

### 9. Import as a Different Name (aliasing specific functions or classes)

Alias specific functions or classes when importing them.

```python
from math import sqrt as square_root 
print(square_root(16))  
# Output: 4.0
```

### 10. Import from a Subpackage

Import modules from **subpackages** within a package.

```python
from mypackage.subpackage import mymodule
```

### 11. Importing Using `__import__`

Dynamically import a module using `__import__`. Generally, `importlib` is preferred for dynamic imports.

```python
module_name = 'math' 
math = __import__(module_name) 
print(math.sqrt(16))  
# Output: 4.0
```

### Examples for a Custom Package Structure

Consider a package structure:

```python
mypackage/     
	__init__.py     
	module1.py     
	module2.py     
	subpackage/         
		__init__.py         
		module3.py
```

**Inside `module1.py`**:

```python
# Import from module2 in the same package 
from . import module2  
# Import from module3 in a subpackage 
from .subpackage import module3
```

**Inside `module3.py`**:

```python
#Import from module1 in the parent package 
from .. import module1
```
### Importing Local Modules

If you have a local script you want to import from, ensure the directory containing the script is in the `sys.path`.

```python
import sys 
sys.path.append('/path/to/your/scripts') 
import your_script
```