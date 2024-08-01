> [! important]
> - Sets have the mathematical operations such as **UNION**, **INTERSECTION**, **DIFFERENCE**, **SYMMETRIC-DIFFERENCE**, **...**
> - Sets remove **DUPLICATES**
> - Sets are not **SUBSCRIPTABLE** (Cannot be indexed like lists)
> - Sets are **UNORDERED**
> - Sets only accepts items that are **HASHABLE** (Tuples, Classes, Callbacks, Integers, Floats, Complexes, Strings, None, Booleans)

## Creating Set

```python
s1 = set() # Creates an empty set
s2 = set([1, 1, 1, True]) # Create a set : {1, True}
```

## Adding elements to a set

> [!note]
> Note that adding an item to a set means that the item will be placed in a random place

```python
s2.add(False) # It will add 'False' to the set
```

## Remove an element from the set

```python
s2.remove(False)
"or"
s2.discard(False)
```

> [!note]
> - **remove(x)** : Will raise an error if the item is not found
> - **discard(x)** : Will not raise an error

## Update the set with another iterable of items

```python
s2.update([5, 6, 10, 10])
# It will be : {1, True, 5, 6, 10}
```

## Union of sets

```python
s1 = {1, 2, 3}
s2 = {3, 4, 5, 6}
print(s1 | s2)
"or"
print(s1.union(s2))
# It will print : {1, 2, 3, 4, 5, 6}
# Removes the duplicates
```

## Intersection of sets

```python
s1 = {1, 2, 3}
s2 = {3, 4, 5, 6}
print(s1 & s2)
"or"
print(s1.intersection(s2))
# It will print : {3}
```

## Difference of sets

> [! note]
> - Difference means items that exists in **s1** and do not exists is **s2**

```python
s1 = {1, 2, 3}
s2 = {3, 4, 5, 6}
print(s1 - s2)
"or"
print(s1.difference(s2))
# It will print : {3}
```

## Symmetric Difference of sets

> [! note]
> - Symmetric Difference means the inverse of the intersection
```python
s1 = {1, 2, 3}
s2 = {3, 4, 5, 6}
print(s1 ^ s2)
"or"
print(s1.symmetric_difference(s2))
# It will print : {3}
```

## Remove a random item and return it

```python
s1 = {1, 2, 3}
print(s1.pop())
# It will print : 1 or 2 or 3 (Because it is a random pick)
```

## Clear a set

```python
s1 = {1, 2, 3}
s1.clear()
print(s1)
# It will print : set()
```

## Copy a set

```python
s1 = {1, 2, 3}
s2 = s1.copy()
```

## Check if a set is a SUPER-SET

> [! important]
> In set theory, a set $A$ is considered a **superset** of another set $B$ if all elements of $B$ are also elements of $A$. This means that $A$ contains all elements of $B$, and possibly more. If $A$ is a superset of $B$, it can be denoted as $A ⊇ B$.

```python
s1 = {1, 2, 3}
s2 = {1, 2}
print(s1.issuperset(s2))
# True
```

## Check if a set is a SUB-SET

> [! important]
> In set theory, a set $A$ is considered a **subset** of another set $B$ if all elements of $A$ are also elements of $B$. This means that $B$ contains all elements of $A$, and possibly more. If $A$ is a subset of $B$, it can be denoted as $B ⊇ A$.

```python
s1 = {1, 2, 3}
s2 = {1, 2}
print(s1.issubset(s2))
# False
```

## Check if two sets are disjoint

> [! important]
> In set theory, a set $A$ and $B$ are considered **DISJOINT**. If their **intersection** is the empty set $\emptyset$

```python
s1 = {1, 2, 3}
s2 = {1, 2}
print(s1.isdisjoint(s2))
# False
```
