> [! important]
> - Dictionaries are HashMaps (K-V paires) stores in a single container and linked by nodes
> - Dictionaries keys can be only of immutable types (int, complex, str, None, bool, tuple, callbacks, classes)
> - Dictionaries ignores duplicating keys
> - Dictionaries values can be of any type

## Creating a dictionary

```python
my_dict1 = dict() # Creates en empty dict
my_dict2 = {} # Also creates an empty dict
my_dict3 = dict([("1", 1)]) # Creates {"1" : 1}
```