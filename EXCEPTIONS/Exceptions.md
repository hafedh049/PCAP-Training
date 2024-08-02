### Base Exception Classes

1. **`BaseException`**: The base class for all built-in exceptions.

   ```python
   class BaseException:
       pass
   ```

2. **`Exception`**: The base class for all non-system-exiting exceptions.

   ```python
   class Exception(BaseException):
       pass
   ```

3. **`ArithmeticError`**: The base class for errors related to arithmetic operations.

   ```python
   class ArithmeticError(Exception):
       pass
   ```

4. **`BufferError`**: Raised when a buffer-related operation fails.

   ```python
   class BufferError(Exception):
       pass
   ```

5. **`LookupError`**: The base class for errors related to looking up items.

   ```python
   class LookupError(Exception):
       pass
   ```

### Arithmetic Errors

1. **`ZeroDivisionError`**: Raised when dividing by zero. $\color{green}\checkmark$

   ```python
   class ZeroDivisionError(ArithmeticError):
       pass
   ```

2. **`OverflowError`**: Raised when an operation exceeds the limits of the numeric type.

   ```python
   class OverflowError(ArithmeticError):
       pass
   ```

3. **`FloatingPointError`**: Raised when a floating-point operation fails.

   ```python
   class FloatingPointError(ArithmeticError):
       pass
   ```

### Lookup Errors $\color{green}\checkmark$

1. **`IndexError`**: Raised when a sequence subscript is out of range. $\color{green}\checkmark$

   ```python
   class IndexError(LookupError):
       pass
   ```

2. **`KeyError`**: Raised when a dictionary key is not found. $\color{green}\checkmark$

   ```python
   class KeyError(LookupError):
       pass
   ```

### File and I/O Errors

1. **`IOError`**: Raised when an I/O operation fails (e.g., file not found). $\color{green}\checkmark$

   ```python
   class IOError(OSError):
       pass
   ```

2. **`FileNotFoundError`**: Raised when a file or directory is requested but cannot be found. $\color{green}\checkmark$

   ```python
   class FileNotFoundError(IOError):
       pass
   ```

3. **`EOFError`**: Raised when the `input()` function hits end-of-file condition.

   ```python
   class EOFError(Exception):
       pass
   ```

4. **`BlockingIOError`**: Raised when an I/O operation would block (non-blocking I/O).

   ```python
   class BlockingIOError(IOError):
       pass
   ```

5. **`ChildProcessError`**: Raised when a child process fails.

   ```python
   class ChildProcessError(OSError):
       pass
   ```

### Syntax and Parsing Errors

1. **`SyntaxError`**: Raised when the parser encounters a syntax error. $\color{green}\checkmark$

   ```python
   class SyntaxError(Exception):
       pass
   ```

2. **`IndentationError`**: Raised for incorrect indentation. $\color{green}\checkmark$

   ```python
   class IndentationError(SyntaxError):
       pass
   ```

3. **`TabError`**: Raised for inconsistent use of tabs and spaces in indentation.

   ```python
   class TabError(IndentationError):
       pass
   ```

### Attribute Errors $\color{green}\checkmark$

1. **`AttributeError`**: Raised when an attribute reference or assignment fails. $\color{green}\checkmark$

   ```python
   class AttributeError(Exception):
       pass
   ```

### Type Errors $\color{green}\checkmark$

1. **`TypeError`**: Raised when an operation or function is applied to an object of inappropriate type. $\color{green}\checkmark$

   ```python
   class TypeError(Exception):
       pass
   ```

### Value Errors $\color{green}\checkmark$

1. **`ValueError`**: Raised when a function receives an argument of the right type but inappropriate value. $\color{green}\checkmark$

   ```python
   class ValueError(Exception):
       pass
   ```

2. **`UnicodeError`**: Raised for errors related to Unicode encoding or decoding.

   ```python
   class UnicodeError(ValueError):
       pass
   ```

### Recursion Errors

**`RecursionError`**: Raised when the maximum recursion depth is exceeded. This error is part of Python’s mechanism to prevent infinite recursion from consuming all available stack space and crashing the interpreter. $\color{green}\checkmark$

```python
class RecursionError(RuntimeError):
    pass
```

### System and Environment Errors

1. **`RuntimeError`**: Raised when an error is detected that doesn’t fall in any of the other categories. $\color{green}\checkmark$

   ```python
   class RuntimeError(Exception):
       pass
   ```

2. **`NotImplementedError`**: Raised by abstract methods to indicate that they need to be implemented in a subclass. $\color{green}\checkmark$

   ```python
   class NotImplementedError(RuntimeError):
       pass
   ```

3. **`ImportError`**: Raised when an imported module cannot be found or loaded. $\color{green}\checkmark$

   ```python
   class ImportError(RuntimeError):
       pass
   ```

4. **`ModuleNotFoundError`**: Raised when a module cannot be found (subclass of `ImportError`). $\color{green}\checkmark$

   ```python
   class ModuleNotFoundError(ImportError):
       pass
   ```

5. **`SystemError`**: Raised when the interpreter detects an internal error.

   ```python
   class SystemError(RuntimeError):
       pass
   ```

6. **`SystemExit`**: Raised by the `sys.exit()` function to exit from Python.

   ```python
   class SystemExit(BaseException):
       pass
   ```

7. **`KeyboardInterrupt`**: Raised when the user hits the interrupt key (usually Ctrl+C).

   ```python
   class KeyboardInterrupt(KeyboardInterrupt):
       pass
   ```

### Warning Exceptions (NOT INCLUDED)

1. **`Warning`**: The base class for all warning categories.

   ```python
   class Warning(Exception):
       pass
   ```

2. **`UserWarning`**: A warning category for user-defined warnings.

   ```python
   class UserWarning(Warning):
       pass
   ```

3. **`DeprecationWarning`**: Raised for deprecated features.

   ```python
   class DeprecationWarning(Warning):
       pass
   ```

4. **`SyntaxWarning`**: Raised for dubious syntax.

   ```python
   class SyntaxWarning(Warning):
       pass
   ```

5. **`RuntimeWarning`**: Raised for runtime issues.

   ```python
   class RuntimeWarning(Warning):
       pass
   ```

6. **`FutureWarning`**: Raised when a feature is planned to change in the future.

   ```python
   class FutureWarning(Warning):
       pass
   ```

7. **`ImportWarning`**: Raised for issues with imports.

   ```python
   class ImportWarning(Warning):
       pass
   ```

8. **`UnicodeWarning`**: Raised for Unicode-related issues.

   ```python
   class UnicodeWarning(Warning):
       pass
   ```

9. **`BytesWarning`**: Raised for bytes-related issues.

   ```python
   class BytesWarning(Warning):
       pass
   ```
