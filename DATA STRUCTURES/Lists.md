A list is an heterogenous array that accepts any types of elements and uses the indexing to access its items.

## Empty List Creation :

```python
my_list1 = list() # This calls the list constructor
my_list2 = [] # Directly initializes an empty list
```

> [!important]
> There is a slight difference between them by the way. The first one creates a list of 10 integers but the second one creates a list that contains the object range()
> ```python
my_list1 = list(range(10)) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
my_list2 = [range(10)] # [range(0, 10, 1)]

## Adding an element :

```python
my_list = [1, 2, 3]
# This method puts the passed element at the en of the list
my_list.append(4) # append() method return 'None'
print(my_list)
# It outputs : [1, 2, 3, 4] 
```

## Extending the list by another ITERABLE :

```python
my_list = [1, 2, 3]
# This method takes the items of the iterable and append the by order one by one at the end of the list
my_list.extend([4, 5, 6]) # extend(x) method return 'None'
print(my_list)
# It outputs : [1, 2, 3, 4, 5, 6] 
```

## Inserting an element at a given position

```python
my_list = [1, 2, 3]
# This method takes index as the first argument and the item to insert
my_list.insert(0, []) # insert(index, item) method return 'None'
print(my_list)
# It outputs : [[], 1, 2, 3] 
```

## Removing an item from the list

```python
my_list = [1, 2, 3]
# This method takes the item to remove as an argument it raises an error if the item is not inside the list
my_list.remove(1) # remove(item) method return 'None'
print(my_list)
# It outputs : [2, 3] 
```

## Removing an item by its index

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
# This method takes the index of the item to remove it also generates an error if index out of range
rm = my_list.pop(-1) # delete the last item and return it
rm = my_list.pop() # delete the last item and return it
rm = my_list.pop(0) # delete the first item and return it
del my_list[0] # delete the first item from the memory
print(my_list, rm)
```

## Clearing the list

```python
my_list = [1, 2, 3]
# This method clears all items of the list
my_list.clear() # clear() method return 'None'
print(my_list)
# It outputs : [] 
```

## Creating a shallow copy from the list

```python
my_list = [1, 2, 3]
my_cp_list = my_list.copy() # copy() method returns a new list that contains all the element of the old list
print(my_cp_list)
# It outputs : [1, 2, 3] 
```

## Counts the occurences of an item

```python
my_list = [1, 1, 1, 1, 2, 3]
nbOc = my_list.count(1) # return the number of occurences of that item
print(nbOc)
# It outputs : 4
```

## Finds the first index from the left of an item

```python
my_list = [1, 1, 1, 1, 2, 3]
indx = my_list.index(2) # return the left first index of that item
print(indx)
# It outputs : 4 (Indexing starts from 0 in PYTHON)
```

## Reversing the list (IN PLACE)

```python
my_list = [1, 2, 3]
my_list.reverse() # return 'None' and reverse the items in-place
print(my_list)
# It outputs : [3,2,1]
```

## Sorting the list (IN PLACE) (TimSort > PowerSort)

```python
my_list = [1, 2, 3]
my_list.sort() # return 'None' and sorts the items in-place, if the items are heterogenous it will fail if you don't provide the 'key' argument (sort criteria) by default it is 'ASC' sort
my_list.sort(reverse = True) # 'DESC' sort
my_list.sort(key: lambda x: x % 2 == 0) # Sorts 'even' numbers first
print(my_list)
# It outputs : [1, 3, 2]
l = [(1, 2), (1, 3)]
l.sort(key=lambda x: x[1], reverse = True)
print(l)
# It outputs : [(1, 3), (1, 2)]
# -----------------------------------------------------------------------
print(sorted(my_list))
```

## List Comprehension

```python
# This is the traditional way to fill a list with items
my_list = []
for i in range(3):
	my_list.append(int(input("Enter a whole number: ")))

# This is called a list comprehension
another_list = [int(input("Enter a number")) for i in range(3)]
```

## Slicing (str, list, tuple)

```python
my_list = [*range(10)]
print(my_list[::]) # It acts as the range and it means select from index 0 to the end of the list with step = 1
# It is the same as : 
print(my_list[0:len(my_list):1])
#-------------------------------------------------------------------------
print(my_list[::-1]) # If the step is negative it means 
# len(my_list) - 1:0:-1, this will show the reversed list 
print([1, 2, 3, 4, 5, 6, 7, 8, 9, 0][-4 : -1])
'''
In this case you should apply the formula of len(l) - x to convert the negative elements (Except the step) to positive because the list is linear
so: 10 - 1 = 9
	10 - 4 = 6
	It will go grom 6 to 9 - 1 (Excluded)
	Therefore [7, 8, 9]
'''
print([1, 2, 3, 4, 5, 6, 7, 8, 9, 0][-1 : -4])
# return [] because you can't go from 9 to 6 and the step is = 1
```