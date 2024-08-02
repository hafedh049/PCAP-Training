The `complex` class in Python provides methods for working with complex numbers, which have a real and an imaginary part. Here is a list of methods for the `complex` class along with examples:

1. **conjugate()**: Returns the complex conjugate of the complex number.
    ```python
    z = 3 + 4j
    print(z.conjugate())  # Output: (3-4j)
    ```

2. **__abs__()**: Returns the magnitude (absolute value) of the complex number.
    ```python
    z = 3 + 4j
    print(z.__abs__())  # Output: 5.0
    ```

3. **__add__(self, other)**: Implements addition of complex numbers.
    ```python
    z1 = 3 + 4j
    z2 = 1 + 2j
    print(z1.__add__(z2))  # Output: (4+6j)
    ```

4. **__bool__()**: Returns `False` if the complex number is zero, `True` otherwise.
    ```python
    z = 0 + 0j
    print(z.__bool__())  # Output: False
    ```

5. **__divmod__(self, other)**: `divmod()` is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        divmod(z, 1 + 1j)
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

6. **__eq__(self, other)**: Implements equality comparison for complex numbers.
    ```python
    z1 = 3 + 4j
    z2 = 3 + 4j
    print(z1.__eq__(z2))  # Output: True
    ```

7. **__floordiv__(self, other)**: Floor division is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        z // 1 + 1j
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

8. **__format__(self, format_spec)**: Formats the complex number according to the given format specification.
    ```python
    z = 3.1415 + 2.718j
    print(z.__format__('.2f'))  # Output: '3.14+2.72j'
    ```

9. **__ge__(self, other)**: Greater than or equal comparison is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z1 = 3 + 4j
        z2 = 1 + 2j
        z1 >= z2
    except TypeError as e:
        print(e)  # Output: '>' not supported between instances of 'complex' and 'complex'
    ```

10. **__gt__(self, other)**: Greater than comparison is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z1 = 3 + 4j
        z2 = 1 + 2j
        z1 > z2
    except TypeError as e:
        print(e)  # Output: '>' not supported between instances of 'complex' and 'complex'
    ```

11. **__hash__()**: Returns the hash value of the complex number.
    ```python
    z = 3 + 4j
    print(z.__hash__())  # Output: -2624276368889032825
    ```

12. **__int__()**: Conversion to `int` is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        int(z)
    except TypeError as e:
        print(e)  # Output: can't convert complex to int
    ```

13. **__le__(self, other)**: Less than or equal comparison is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z1 = 3 + 4j
        z2 = 1 + 2j
        z1 <= z2
    except TypeError as e:
        print(e)  # Output: '<=' not supported between instances of 'complex' and 'complex'
    ```

14. **__lt__(self, other)**: Less than comparison is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z1 = 3 + 4j
        z2 = 1 + 2j
        z1 < z2
    except TypeError as e:
        print(e)  # Output: '<' not supported between instances of 'complex' and 'complex'
    ```

15. **__mod__(self, other)**: Modulo operation is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        z % 1 + 1j
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

16. **__mul__(self, other)**: Implements multiplication of complex numbers.
    ```python
    z1 = 3 + 4j
    z2 = 1 + 2j
    print(z1.__mul__(z2))  # Output: (-5+10j)
    ```

17. **__ne__(self, other)**: Implements inequality comparison for complex numbers.
    ```python
    z1 = 3 + 4j
    z2 = 1 + 2j
    print(z1.__ne__(z2))  # Output: True
    ```

18. **__neg__()**: Implements unary negation for complex numbers.
    ```python
    z = 3 + 4j
    print(z.__neg__())  # Output: (-3 -4j)
    ```

19. **__pos__()**: Implements unary positive (returns the value itself).
    ```python
    z = 3 + 4j
    print(z.__pos__())  # Output: (3 + 4j)
    ```

20. **__pow__(self, other, modulo=None)**: Implements power function for complex numbers.
    ```python
    z = 3 + 4j
    print(z.__pow__(2))  # Output: (-7 + 24j)
    ```

21. **__radd__(self, other)**: Implements reverse addition.
    ```python
    z = 3 + 4j
    print((2).__radd__(z))  # Output: (5 + 4j)
    ```

22. **__rdivmod__(self, other)**: `divmod()` is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        divmod(1 + 1j, z)
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

23. **__rfloordiv__(self, other)**: Floor division is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        (1 + 1j) // z
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

24. **__rmod__(self, other)**: Modulo operation is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        (1 + 1j) % z
    except TypeError as e:
        print(e)  # Output: can't take floor or mod of complex number.
    ```

25. **__rmul__(self, other)**: Implements reverse multiplication.
    ```python
    z = 3 + 4j
    print((2).__rmul__(z))  # Output: (6+8j)
    ```

26. **__round__(self, ndigits=None)**: Rounding is not supported for complex numbers and will raise a `TypeError`.
    ```python
    try:
        z = 3 + 4j
        round(z)
    except TypeError as e:
        print(e)  # Output: type complex doesn't define __round__ method
    ```

27. **__rpow__(self, other)**: Implements reverse power function.
    ```python
    z = 3 + 4j
    print((2).__rpow__(z))  
    # Output: (-0.4196079565772849 -0.9072292643081347j)
    ```

28. **__rsub__(self, other)**: Implements reverse subtraction.
    ```python
    z = 3 + 4j
    print((2).__rsub__(z))  # Output: (-1 -4j)
    ```
```
