The `int` class in Python has a smaller set of methods compared to the `str` class. Here is a list of methods for the `int` class along with examples:

1. **bit_length()**: Returns the number of bits necessary to represent the integer in binary.
    ```python
    print((10).bit_length())  # Output: 4
    ```

2. **conjugate()**: Returns the complex conjugate of the integer. Since integers are real numbers, it returns the integer itself.
    ```python
    print((10).conjugate())  # Output: 10
    ```

3. **from_bytes(bytes, byteorder, *, signed=False)**: Returns an integer from the given array of bytes.
    ```python
    bytes_value = b'\x00\x0a'
    print(int.from_bytes(bytes_value, byteorder='big'))  # Output: 10
    ```

4. **to_bytes(length, byteorder, *, signed=False)**: Returns an array of bytes representing the integer.
    ```python
    print((10).to_bytes(2, byteorder='big'))  # Output: b'\x00\x0a'
    ```

5. **as_integer_ratio()**: Returns a pair of integers, whose ratio is exactly equal to the original integer and with a positive denominator.
    ```python
    print((10).as_integer_ratio())  # Output: (10, 1)
    ```

6. **__abs__()**: Returns the absolute value of the integer.
    ```python
    print((10).__abs__())  # Output: 10
    ```

7. **__add__(self, other)**: Implements addition.
    ```python
    print((10).__add__(5))  # Output: 15
    ```

8. **__and__(self, other)**: Implements bitwise AND.
    ```python
    print((10).__and__(7))  # Output: 2
    ```

9. **__bool__()**: Returns `False` if the integer is zero, `True` otherwise.
    ```python
    print((10).__bool__())  # Output: True
    ```

10. **__ceil__()**: Returns the ceiling value of the integer (integer itself).
    ```python
    import math
    print((10).__ceil__())  # Output: 10
    ```

11. **__divmod__(self, other)**: Implements the `divmod()` function.
    ```python
    print((10).__divmod__(3))  # Output: (3, 1)
    ```

12. **__eq__(self, other)**: Implements equality comparison.
    ```python
    print((10).__eq__(10))  # Output: True
    ```

13. **__float__()**: Converts the integer to a float.
    ```python
    print((10).__float__())  # Output: 10.0
    ```

14. **__floor__()**: Returns the floor value of the integer (integer itself).
    ```python
    import math
    print((10).__floor__())  # Output: 10
    ```

15. **__floordiv__(self, other)**: Implements integer (floor) division.
    ```python
    print((10).__floordiv__(3))  # Output: 3
    ```

16. **__format__(self, format_spec)**: Formats the integer according to the given format specification.
    ```python
    print((10).__format__('x'))  # Output: 'a'
    ```

17. **__ge__(self, other)**: Implements greater than or equal comparison.
    ```python
    print((10).__ge__(5))  # Output: True
    ```

18. **__gt__(self, other)**: Implements greater than comparison.
    ```python
    print((10).__gt__(5))  # Output: True
    ```

19. **__hash__()**: Returns the hash value of the integer.
    ```python
    print((10).__hash__())  # Output: 10
    ```

20. **__index__()**: Returns the integer itself. This is used for slicing operations.
    ```python
    print((10).__index__())  # Output: 10
    ```

21. **__int__()**: Converts the value to an integer (identity function for integers).
    ```python
    print((10).__int__())  # Output: 10
    ```

22. **__invert__()**: Implements bitwise inversion.
    ```python
    print((10).__invert__())  # Output: -11
    ```

23. **__le__(self, other)**: Implements less than or equal comparison.
    ```python
    print((10).__le__(10))  # Output: True
    ```

24. **__lshift__(self, other)**: Implements bitwise left shift.
    ```python
    print((10).__lshift__(2))  # Output: 40
    ```

25. **__lt__(self, other)**: Implements less than comparison.
    ```python
    print((10).__lt__(5))  # Output: False
    ```

26. **__mod__(self, other)**: Implements modulo operation.
    ```python
    print((10).__mod__(3))  # Output: 1
    ```

27. **__mul__(self, other)**: Implements multiplication.
    ```python
    print((10).__mul__(5))  # Output: 50
    ```

28. **__ne__(self, other)**: Implements inequality comparison.
    ```python
    print((10).__ne__(5))  # Output: True
    ```

29. **__neg__()**: Implements unary negation.
    ```python
    print((10).__neg__())  # Output: -10
    ```

30. **__or__(self, other)**: Implements bitwise OR.
    ```python
    print((10).__or__(5))  # Output: 15
    ```

31. **__pos__()**: Implements unary positive (returns the value itself).
    ```python
    print((10).__pos__())  # Output: 10
    ```

32. **__pow__(self, other, modulo=None)**: Implements power function.
    ```python
    print((10).__pow__(2))  # Output: 100
    print((10).__pow__(2, 7))  # Output: 2 (100 % 7)
    ```

33. **__radd__(self, other)**: Implements reverse addition.
    ```python
    print((10).__radd__(5))  # Output: 15
    ```

34. **__rand__(self, other)**: Implements reverse bitwise AND.
    ```python
    print((10).__rand__(7))  # Output: 2
    ```

35. **__rfloordiv__(self, other)**: Implements reverse floor division.
    ```python
    print((10).__rfloordiv__(3))  # Output: 0
    ```

36. **__rlshift__(self, other)**: Implements reverse left shift.
    ```python
    print((10).__rlshift__(2))  # Output: 40
    ```

37. **__rmod__(self, other)**: Implements reverse modulo.
    ```python
    print((10).__rmod__(3))  # Output: 3
    ```

38. **__rmul__(self, other)**: Implements reverse multiplication.
    ```python
    print((10).__rmul__(5))  # Output: 50
    ```

39. **__ror__(self, other)**: Implements reverse bitwise OR.
    ```python
    print((10).__ror__(5))  # Output: 15
    ```

40. **__round__(self, ndigits=None)**: Rounds the integer (identity function for integers).
    ```python
    print((10).__round__())  # Output: 10
    ```

41. **__rpow__(self, other, modulo=None)**: Implements reverse power function.
    ```python
    print((10).__rpow__(2))  # Output: 1024
    ```

42. **__rrshift__(self, other)**: Implements reverse right shift.
    ```python
    print((10).__rrshift__(2))  # Output: 2
    ```

43. **__rshift__(self, other)**: Implements bitwise right shift.
    ```python
    print((10).__rshift__(2))  # Output: 2
    ```

44. **__rsub__(self, other)**: Implements reverse subtraction.
    ```python
    print((10).__rsub__(5))  # Output: -5
    ```

45. **__rtruediv__(self, other)**: Implements reverse true division.
    ```python
    print((10).__rtruediv__(2))  # Output: 0.2
    ```

46. **__rxor__(self, other)**: Implements reverse bitwise XOR.
    ```python
    print((10).__rxor__(5))  # Output: 15
    ```

47. **__sub__(self, other)**: Implements subtraction.
    ```python
    print((10).__sub__(5))  # Output: 5
    ```

48. **__truediv__(self, other)**: Implements true division.
    ```python
    print((10).__truediv__(4))  # Output: 2.5
    ```

49. **__trunc__()**: Truncates the integer (identity function for integers).
    ```python
    import math
    print((10).__trunc__())  # Output: 10
    ```

50. **__xor__(self, other)**: Implements bitwise XOR.
    ```python
    print((10).__xor__(5))  # Output: 15
    ```
