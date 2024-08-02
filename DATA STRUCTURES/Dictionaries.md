> [! important]
> - Dictionaries are HashMaps (K-V paires) stores in a single container and linked by nodes
> - Dictionaries keys can be only of immutable types **(int, complex, str, None, bool, tuple, callbacks, classes, frozensets)**
> - Dictionaries ignores duplicating keys
> - Dictionaries values can be of any type

## Creating a dictionary

```python
my_dict1 = dict() # Creates en empty dict
my_dict2 = {} # Also creates an empty dict
my_dict3 = dict([("1", 1)]) # Creates {"1" : 1}
```

In Python, dictionaries (`dict`) have a variety of methods that allow you to manipulate and query the dictionary in various ways. Here’s a comprehensive list of dictionary methods along with examples for each:

### Dictionary Methods

1. **`dict.clear()`**
   - Removes all items from the dictionary.

   ```python
   my_dict = {'a': 1, 'b': 2}
   my_dict.clear()
   print(my_dict)  # Output: {}
   ```

2. **`dict.copy()`**
   - Returns a shallow copy of the dictionary.

   ```python
   my_dict = {'a': 1, 'b': 2}
   copied_dict = my_dict.copy()
   print(copied_dict)  # Output: {'a': 1, 'b': 2}
   ```

3. **`dict.fromkeys(seq, value)`**
   - Creates a new dictionary with keys from `seq` and values set to `value`.

   ```python
   keys = ('a', 'b', 'c')
   new_dict = dict.fromkeys(keys, 0)
   print(new_dict)  # Output: {'a': 0, 'b': 0, 'c': 0}
   ```

4. **`dict.get(key, default)`**
   - Returns the value for `key` if `key` is in the dictionary; otherwise, returns `default`.

   ```python
   my_dict = {'a': 1, 'b': 2}
   print(my_dict.get('a'))         # Output: 1
   print(my_dict.get('c', 'Not Found'))  # Output: Not Found
   ```

5. **`dict.items()`**
   - Returns a view object that displays a list of a dictionary’s key-value tuple pairs.

   ```python
   my_dict = {'a': 1, 'b': 2}
   print(list(my_dict.items()))  # Output: [('a', 1), ('b', 2)]
   ```

6. **`dict.keys()`**
   - Returns a view object that displays a list of all the keys in the dictionary.

   ```python
   my_dict = {'a': 1, 'b': 2}
   print(list(my_dict.keys()))  # Output: ['a', 'b']
   ```

7. **`dict.pop(key, default)`**
   - Removes the specified key and returns the corresponding value. If the key is not found, returns `default` if provided.

   ```python
   my_dict = {'a': 1, 'b': 2}
   print(my_dict.pop('a'))  # Output: 1
   print(my_dict.pop('c', 'Not Found'))  # Output: Not Found
   print(my_dict)  # Output: {'b': 2}
   ```

8. **`dict.popitem()`**
   - Removes and returns the last key-value pair as a tuple.

   ```python
   my_dict = {'a': 1, 'b': 2}
   print(my_dict.popitem())  # Output: ('b', 2) (order might vary)
   print(my_dict)  # Output: {'a': 1}
   ```

9. **`dict.setdefault(key, default)`**
   - Returns the value of `key` if `key` is in the dictionary. If not, inserts `key` with a value of `default` and returns `default`.

   ```python
   my_dict = {'a': 1}
   print(my_dict.setdefault('b', 2))  # Output: 2
   print(my_dict.setdefault('a', 3))  # Output: 1 (existing value)
   print(my_dict)  # Output: {'a': 1, 'b': 2}
   ```

10. **`dict.update(other)`**
    - Updates the dictionary with elements from another dictionary or from an iterable of key-value pairs.

    ```python
    my_dict = {'a': 1}
    my_dict.update({'b': 2, 'c': 3})
    print(my_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
    "or"
    my_dict["d"] = [1, 2, 3]
    ```

11. **`dict.values()`**
    - Returns a view object that displays a list of all the values in the dictionary.

    ```python
    my_dict = {'a': 1, 'b': 2}
    print(list(my_dict.values()))  # Output: [1, 2]
    ```

12. **`dict.setdefault(key, default)`**
    - Similar to `get()`, but also sets the `default` if `key` is not already in the dictionary.

    ```python
    my_dict = {'a': 1}
    print(my_dict.setdefault('b', 2))  # Output: 2
    print(my_dict)  # Output: {'a': 1, 'b': 2}
    ```
