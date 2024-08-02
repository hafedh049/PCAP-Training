The `frozenset` type in Python represents an immutable version of a set. It provides many of the same set operations as a regular `set`, but since it is immutable, it does not support methods that modify the set. Here’s a list of all the methods available for `frozenset`, along with examples:

### frozenset Methods

1. **`frozenset.copy()`**
   - Returns a shallow copy of the `frozenset`. Since `frozenset` is immutable, this method is redundant but still available.

   ```python
   fs = frozenset([1, 2, 3])
   copy_fs = fs.copy()
   print(copy_fs)  # Output: frozenset({1, 2, 3})
   ```

2. **`frozenset.difference(*others)`**
   - Returns a new `frozenset` with elements in the original `frozenset` but not in the other `frozensets`.

   ```python
   fs1 = frozenset([1, 2, 3])
   fs2 = frozenset([2, 3, 4])
   diff_fs = fs1.difference(fs2)
   print(diff_fs)  # Output: frozenset({1})
   ```

3. **`frozenset.difference_update(*others)`**
   - This method is not available for `frozenset` because it would require modifying the set.

4. **`frozenset.discard(elem)`**
   - This method is not available for `frozenset` because it would require modifying the set.

5. **`frozenset.intersection(*others)`**
   - Returns a new `frozenset` with elements common to all `frozensets`.

   ```python
   fs1 = frozenset([1, 2, 3])
   fs2 = frozenset([2, 3, 4])
   inter_fs = fs1.intersection(fs2)
   print(inter_fs)  # Output: frozenset({2, 3})
   ```

6. **`frozenset.intersection_update(*others)`**
   - This method is not available for `frozenset` because it would require modifying the set.

7. **`frozenset.isdisjoint(other)`**
   - Returns `True` if the `frozenset` has no elements in common with `other`.

   ```python
   fs1 = frozenset([1, 2, 3])
   fs2 = frozenset([4, 5, 6])
   print(fs1.isdisjoint(fs2))  # Output: True
   ```

8. **`frozenset.issubset(other)`**
   - Returns `True` if all elements of the `frozenset` are in `other`.

   ```python
   fs1 = frozenset([1, 2])
   fs2 = frozenset([1, 2, 3])
   print(fs1.issubset(fs2))  # Output: True
   ```

9. **`frozenset.issuperset(other)`**
   - Returns `True` if all elements of `other` are in the `frozenset`.

   ```python
   fs1 = frozenset([1, 2, 3])
   fs2 = frozenset([1, 2])
   print(fs1.issuperset(fs2))  # Output: True
   ```

10. **`frozenset.pop()`**
    - This method is not available for `frozenset` because it would require modifying the set.

11. **`frozenset.remove(elem)`**
    - This method is not available for `frozenset` because it would require modifying the set.

12. **`frozenset.symmetric_difference(other)`**
    - Returns a new `frozenset` with elements in either the `frozenset` or `other` but not both.

    ```python
    fs1 = frozenset([1, 2, 3])
    fs2 = frozenset([2, 3, 4])
    sym_diff_fs = fs1.symmetric_difference(fs2)
    print(sym_diff_fs)  # Output: frozenset({1, 4})
    ```

13. **`frozenset.symmetric_difference_update(other)`**
    - This method is not available for `frozenset` because it would require modifying the set.

14. **`frozenset.union(*others)`**
    - Returns a new `frozenset` with elements from the `frozenset` and all others.

    ```python
    fs1 = frozenset([1, 2])
    fs2 = frozenset([2, 3])
    union_fs = fs1.union(fs2)
    print(union_fs)  # Output: frozenset({1, 2, 3})
    ```

15. **`frozenset.update(*others)`**
    - This method is not available for `frozenset` because it would require modifying the set.

16. **`frozenset.__contains__(elem)`**
    - Returns `True` if `elem` is in the `frozenset`.

    ```python
    fs = frozenset([1, 2, 3])
    print(1 in fs)  # Output: True
    print(4 in fs)  # Output: False
    ```

17. **`frozenset.__iter__()`**
    - Returns an iterator over the `frozenset`.

    ```python
    fs = frozenset([1, 2, 3])
    for elem in fs:
        print(elem)  # Output: 1 2 3 (order might vary)
    ```

18. **`frozenset.__len__()`**
    - Returns the number of elements in the `frozenset`.

    ```python
    fs = frozenset([1, 2, 3])
    print(len(fs))  # Output: 3
    ```
