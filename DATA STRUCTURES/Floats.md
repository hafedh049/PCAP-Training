The `float` class in Python has a set of methods that allow you to work with floating-point numbers. Here is a list of methods for the `float` class along with examples:

1. **as_integer_ratio()**: Returns a pair of integers, whose ratio is exactly equal to the original float and with a positive denominator.
    ```python
    print((10.5).as_integer_ratio())  # Output: (21, 2)
    ```

2. **conjugate()**: Returns the complex conjugate of the float. Since floats are real numbers, it returns the float itself.
    ```python
    print((10.5).conjugate())  # Output: 10.5
    ```

3. **fromhex(s)**: Returns a float represented by a hexadecimal string s.
    ```python
    print(float.fromhex('0x1.4p2'))  # Output: 5.0
    ```

4. **hex()**: Returns a string representing the float in hexadecimal.
    ```python
    print((5.0).hex())  # Output: '0x1.4p2'
    ```

5. **is_integer()**: Returns `True` if the float is an integer.
    ```python
    print((10.0).is_integer())  # Output: True
    print((10.5).is_integer())  # Output: False
    ```

6. **__abs__()**: Returns the absolute value of the float.
    ```python
    print((10.5).__abs__())  # Output: 10.5
    ```

7. **__add__(self, other)**: Implements addition.
    ```python
    print((10.5).__add__(2.5))  # Output: 13.0
    ```

8. **__bool__()**: Returns `False` if the float is zero, `True` otherwise.
    ```python
    print((10.5).__bool__())  # Output: True
    ```

9. **__divmod__(self, other)**: Implements the `divmod()` function.
    ```python
    print((10.5).__divmod__(2.5))  # Output: (4.0, 0.5)
    ```

10. **__eq__(self, other)**: Implements equality comparison.
    ```python
    print((10.5).__eq__(10.5))  # Output: True
    ```

11. **__float__()**: Converts the value to a float (identity function for floats).
    ```python
    print((10.5).__float__())  # Output: 10.5
    ```

12. **__floordiv__(self, other)**: Implements integer (floor) division.
    ```python
    print((10.5).__floordiv__(2.5))  # Output: 4.0
    ```

13. **__format__(self, format_spec)**: Formats the float according to the given format specification.
    ```python
    print((10.5).__format__('.2f'))  # Output: '10.50'
    ```

14. **__ge__(self, other)**: Implements greater than or equal comparison.
    ```python
    print((10.5).__ge__(5.0))  # Output: True
    ```

15. **__gt__(self, other)**: Implements greater than comparison.
    ```python
    print((10.5).__gt__(5.0))  # Output: True
    ```

16. **__hash__()**: Returns the hash value of the float.
    ```python
    print((10.5).__hash__())  # Output: 1152921504606846986
    ```

17. **__int__()**: Converts the float to an integer (truncates towards zero).
    ```python
    print((10.5).__int__())  # Output: 10
    ```

18. **__le__(self, other)**: Implements less than or equal comparison.
    ```python
    print((10.5).__le__(10.5))  # Output: True
    ```

19. **__lt__(self, other)**: Implements less than comparison.
    ```python
    print((10.5).__lt__(5.0))  # Output: False
    ```

20. **__mod__(self, other)**: Implements modulo operation.
    ```python
    print((10.5).__mod__(2.5))  # Output: 0.5
    ```

21. **__mul__(self, other)**: Implements multiplication.
    ```python
    print((10.5).__mul__(2.0))  # Output: 21.0
    ```

22. **__ne__(self, other)**: Implements inequality comparison.
    ```python
    print((10.5).__ne__(5.0))  # Output: True
    ```

23. **__neg__()**: Implements unary negation.
    ```python
    print((10.5).__neg__())  # Output: -10.5
    ```

24. **__pos__()**: Implements unary positive (returns the value itself).
    ```python
    print((10.5).__pos__())  # Output: 10.5
    ```

25. **__pow__(self, other, modulo=None)**: Implements power function.
    ```python
    print((10.5).__pow__(2))  # Output: 110.25
    ```

26. **__radd__(self, other)**: Implements reverse addition.
    ```python
    print((10.5).__radd__(2.5))  # Output: 13.0
    ```

27. **__rdivmod__(self, other)**: Implements reverse `divmod()`.
    ```python
    print((2.5).__rdivmod__(10.5))  # Output: (4.0, 0.5)
    ```

28. **__rfloordiv__(self, other)**: Implements reverse floor division.
    ```python
    print((2.5).__rfloordiv__(10.5))  # Output: 4.0
    ```

29. **__rmod__(self, other)**: Implements reverse modulo.
    ```python
    print((2.5).__rmod__(10.5))  # Output: 0.5
    ```

30. **__rmul__(self, other)**: Implements reverse multiplication.
    ```python
    print((2.0).__rmul__(10.5))  # Output: 21.0
    ```

31. **__round__(self, ndigits=None)**: Rounds the float to the nearest integer, or to a specified number of decimal places.
    ```python
    print((10.5).__round__())  # Output: 10
    print((10.5678).__round__(2))  # Output: 10.57
    ```

32. **__rpow__(self, other)**: Implements reverse power function.
    ```python
    print((2.0).__rpow__(10.5))  # Output: 148.4131591025766
    ```

33. **__rsub__(self, other)**: Implements reverse subtraction.
    ```python
    print((2.5).__rsub__(10.5))  # Output: 8.0
    ```

34. **__rtruediv__(self, other)**: Implements reverse true division.
    ```python
    print((2.5).__rtruediv__(10.5))  # Output: 4.2
    ```

35. **__sub__(self, other)**: Implements subtraction.
    ```python
    print((10.5).__sub__(2.5))  # Output: 8.0
    ```

36. **__truediv__(self, other)**: Implements true division.
    ```python
    print((10.5).__truediv__(2.5))  # Output: 4.2
    ```
    