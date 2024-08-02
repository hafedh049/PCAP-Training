In Python, the `str` class has numerous methods that allow you to manipulate strings. Here's a comprehensive list of the methods along with examples:

## Creating a string

```python
ch1 = str() # Creates an empty string
ch2 = str([]) # Convert [] to '[]'
ch3 = "123";
ch4 = '000'
ch5 = '''+++'''
ch6 = """Hello World"""
```

1. **capitalize()**: Converts the first character to uppercase.
    ```python
    print("hello".capitalize())  # Output: "Hello"
    ```

2. **casefold()**: Converts the string to lowercase for caseless matching.
    ```python
    print("HELLO".casefold())  # Output: "hello"
    ```

3. **center(width, fillchar)**: Centers the string in a field of a given width.
    ```python
    print("hello".center(10, '-'))  # Output: "--hello---"
    ```

4. **count(subs[, start, end])**: Counts occurrences of a substring.
    ```python
    print("hello".count('l'))  # Output: 2
    ```

5. **encode(encoding, errors)**: Encodes the string to bytes.
    ```python
    print("hello".encode())  # Output: b'hello'
    ```

6. **endswith(suffix, start, end)**: Checks if the string ends with a specified suffix.
    ```python
    print("hello".endswith('o'))  # Output: True
    ```

7. **expandtabs(tabsize)**: Replaces tabs with spaces.
    ```python
    print("hello\tworld".expandtabs(4))  # Output: "hello   world"
    ```

8. **find(sub, start, end)**: Finds the first occurrence of a substring.
    ```python
    print("hello".find('l'))  # Output: 2
    ```

9. **format(*args, **kwargs)**: Formats the string.
    ```python
    print("Hello, {}".format("world"))  # Output: "Hello, world"
    ```

10. **format_map(mapping)**: Formats the string using a mapping.
```python
print("{name} is {age} years old".format_map({'name': 'Alice', 'age': 30}))  # Output: "Alice is 30 years old"
```

11. **index(sub, start, end)**: Finds the first occurrence of a substring (raises an error if not found).
    ```python
    print("hello".index('l'))  # Output: 2
    ```

12. **isalnum()**: Checks if all characters are alphanumeric.
    ```python
    print("hello123".isalnum())  # Output: True
    ```

13. **isalpha()**: Checks if all characters are alphabetic.
    ```python
    print("hello".isalpha())  # Output: True
    ```

14. **isascii()**: Checks if all characters are ASCII.
    ```python
    print("hello".isascii())  # Output: True
    ```

15. **isdecimal()**: Checks if all characters are decimals.
    ```python
    print("123".isdecimal())  # Output: True
    ```

16. **isdigit()**: Checks if all characters are digits.
    ```python
    print("123".isdigit())  # Output: True
    ```

17. **isidentifier()**: Checks if the string is a valid identifier.
    ```python
    print("hello".isidentifier())  # Output: True
    ```

18. **islower()**: Checks if all characters are lowercase.
    ```python
    print("hello".islower())  # Output: True
    ```

19. **isnumeric()**: Checks if all characters are numeric.
    ```python
    print("123".isnumeric())  # Output: True
    ```

20. **isprintable()**: Checks if all characters are printable.
    ```python
    print("hello".isprintable())  # Output: True
    ```

21. **isspace()**: Checks if all characters are whitespace.
    ```python
    print("   ".isspace())  # Output: True
    ```

22. **istitle()**: Checks if the string is title-cased.
    ```python
    print("Hello World".istitle())  # Output: True
    ```

23. **isupper()**: Checks if all characters are uppercase.
    ```python
    print("HELLO".isupper())  # Output: True
    ```

24. **join(iterable)**: Joins elements of an iterable with the string as a separator.
    ```python
    print(",".join(["a", "b", "c"]))  # Output: "a,b,c"
    ```

25. **ljust(width, fillchar)**: Left-justifies the string in a field of a given width.
    ```python
    print("hello".ljust(10, '-'))  # Output: "hello-----"
    ```

26. **lower()**: Converts the string to lowercase.
    ```python
    print("HELLO".lower())  # Output: "hello"
    ```

27. **lstrip(chars)**: Strips leading characters.
    ```python
    print("   hello".lstrip())  # Output: "hello"
    ```

28. **maketrans(x, y, z)**: Returns a translation table to be used with `translate()`.
    ```python
    table = str.maketrans('aeiou', '12345')
    print("hello".translate(table))  # Output: "h2ll4"
    ```

29. **partition(sep)**: Partitions the string into a 3-tuple around a separator.
    ```python
    print("hello world".partition(" "))  # Output: ("hello", " ", "world")
    ```

30. **replace(old, new, count)**: Replaces occurrences of a substring with another.
    ```python
    print("hello world".replace("world", "Python"))  # Output: "hello Python"
    ```

31. **rfind(sub, start, end)**: Finds the last occurrence of a substring.
    ```python
    print("hello".rfind('l'))  # Output: 3
    ```

32. **rindex(sub, start, end)**: Finds the last occurrence of a substring (raises an error if not found).
    ```python
    print("hello".rindex('l'))  # Output: 3
    ```

33. **rjust(width, fillchar)**: Right-justifies the string in a field of a given width.
    ```python
    print("hello".rjust(10, '-'))  # Output: "-----hello"
    ```

34. **rpartition(sep)**: Partitions the string into a 3-tuple around a separator (starting from the end).
    ```python
    print("hello world".rpartition(" "))  # Output: ("hello", " ", "world")
    ```

35. **rsplit(sep, maxsplit)**: Splits the string from the end.
    ```python
    print("hello world".rsplit(" "))  # Output: ["hello", "world"]
    ```

36. **rstrip(chars)**: Strips trailing characters.
    ```python
    print("hello   ".rstrip())  # Output: "hello"
    ```

37. **split(sep, maxsplit)**: Splits the string.
    ```python
    print("hello world".split(" "))  # Output: ["hello", "world"]
    ```

38. **splitlines(keepends)**: Splits the string at line breaks.
    ```python
    print("hello\nworld".splitlines())  # Output: ["hello", "world"]
    ```

39. **startswith(prefix, start, end)**: Checks if the string starts with a specified prefix.
    ```python
    print("hello".startswith('h'))  # Output: True
    ```

40. **strip(chars)**: Strips leading and trailing characters.
    ```python
    print("   hello   ".strip())  # Output: "hello"
    ```

41. **swapcase()**: Swaps case, lower becomes upper and vice versa.
    ```python
    print("Hello".swapcase())  # Output: "hELLO"
    ```

42. **title()**: Converts the first character of each word to uppercase.
    ```python
    print("hello world".title())  # Output: "Hello World"
    ```

43. **translate(table)**: Translates the string using a translation table.
    ```python
    table = str.maketrans('aeiou', '12345')
    print("hello".translate(table))  # Output: "h2ll4"
    ```

44. **upper()**: Converts the string to uppercase.
    ```python
    print("hello".upper())  # Output: "HELLO"
    ```

45. **zfill(width[, char = "0"])**: Pads the string with zeros on the left to a specified width.
    ```python
    print("42".zfill(5,"0"))  # Output: "00042"
    ```

These methods provide a rich set of tools for working with strings in Python.