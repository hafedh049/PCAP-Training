### Example of Handling Exceptions

```python
def divide_numbers(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Error: Cannot divide by zero.")
        return None
    except TypeError:
        print("Error: Invalid input type. Both arguments must be numbers.")
        return None
    except Exception as e:
	    pass
	    ...
	    print(e)
    else:
        print(f"The result is: {result}")
        return result
    finally:
        print("Execution completed.")

"Exception is from specific to general (subs > sups)"

divide_numbers(10, 2)  # Normal case
divide_numbers(10, 0)  # ZeroDivisionError case
divide_numbers(10, 'a')  # TypeError case
```

![[Pasted image 20240802115214.png]]

In this example:
- **`ZeroDivisionError`** is caught when attempting to divide by zero.
- **`TypeError`** is caught when the input types are incorrect.
- **`else`** block executes if no exceptions are raised.
- **`finally`** block executes regardless of whether an exception was raised or not.

### Example of Custom Exception Classes

You can define custom exception classes to handle specific error conditions in your application. Here's how to create and use custom exception classes:

```python
class ValidationError(Exception):
    def __init__(self, message):
        super().__init__(message)
        self.message = message

class DivisionByZeroError(ValidationError):
    def __init__(self):
        super().__init__("Division by zero is not allowed.")

class InvalidInputError(ValidationError):
    def __init__(self, input_type):
        super().__init__(f"Invalid input type: {input_type}. Expected a number.")

def divide_numbers_custom(a, b):
    if not isinstance(a, (int, float)) or not isinstance(b, (int, float)):
        raise InvalidInputError(type(a).__name__)
    if b == 0:
        raise DivisionByZeroError()
    
    result = a / b
    print(f"The result is: {result}")
    return result

try:
    divide_numbers_custom(10, 2)  # Normal case
    divide_numbers_custom(10, 0)  # DivisionByZeroError case
    divide_numbers_custom(10, 'a')  # InvalidInputError case
except ValidationError as e:
    print("Caught a ValidationError:", e)
```

In this example:
- **Custom exceptions** `ValidationError`, `DivisionByZeroError`, and `InvalidInputError` are defined to handle specific error conditions.
- **`divide_numbers_custom`** function raises these custom exceptions based on the input conditions.
- **`try-except`** block catches the custom exceptions and handles them appropriately.

> [!important]
> - **'try'** block must be either with **finally** or with **except** or with both but not with **else**
> - **'else'** is executed if there is no exception
> - **'finally'** is executed no matter what happens even if you call **'return'**, **'quit()'** or **'exit()'** 
> - except hierarchy must be from **specific** to **general**
