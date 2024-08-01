**Ranges** are a **sequence** of **integers** or **floats**

```python
# This will create a sequence of integers from 0 to 9 with step = 1  
my_range1 = range(10)
# This will create a sequence of integers from 10 to 19 with step = 1  
my_range2 = range(10,20)
# This will create a sequence of integers from 10 to 99 with step = 10
# 10,20,30,40,50,60,70,80 it will not reach 100 as 100 is excluded from the range
my_range3 = range(10,100,10)
```

> [!important]
> General Formula for the range is:
> 	range(a,b,c) = a sequence from a to b - 1 with step = c

> [!important]
> At least you need to provide one argument to the range
> - If **one** argument is set to the range the that argument is the **END** and it will start from 0
> - If **two** arguments are set the a is the **START** and b is the **END**
> - If **three** arguments are set the the third one which is **c** is the **STEP** and if **ommited** it will be **1** by **default**

## Examples :

```python
print(*range(10))
print(*range(3,9))
print(*range(20,29,3))
print(*range(-1,-5))
print(*range(-10,-30,-3))
```

## Methods & Attributes

```python
my_range = range(10)
print(my_range.count(0)) # Outputs: 1
print(my_range.index(0)) # Outputs: 0

print(my_range.start) # Outputs: 0
print(my_range.stop) # Outputs: 10
print(my_range.step) # Outputs: 1
```