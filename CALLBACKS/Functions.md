## Defining a function :

```python
def my_func():
	...
# This is a function called 'my_func' and it has no parameters and no body
# By default if there is no return inside the callback it will return 'None'

def fib(n):
	if n in [0,1]:
		return 1
	else:
		return fib(n - 1) + fib(n - 2)
# This is a recursive fibonacci function

def f(x,y,*args,*kwargs, z = None):
	...

f(1, 2, [], "", a = 12, z = None)

# x and y are called required arguments 
# *args means that i cant put 0 or many simple arguments
# **kwargs means that i can put 0 or many optional | keyword arguments
# *args is a tuple and **kwargs is a dictionary
```

## Nesting functions :

```python
def f(a):
	def g(b)
		return a + b
	return g

x = 56
f1 = f(56)
print(f1(33))
# Outputs 56 + 33 > 89
```

## Local and Global Variables :

```python
a = 5

def fn():
	global a
	b = 4
	print(a := 10)
	
fn()
# Outputs : 10 
# := operator is called wallrus operator it creates, assigns and return the variable
# a is global and b is local
"-------------------------------------------------------------------------"
a = 4

def f():
    a = 10
    
    def ff():
        nonlocal a
        print(a)
    
    ff()

f()
# nonlocal tells python i don't want the global 'a' i want the nearest local variable called 'a' but not in my scope
```

## Lambdas :

```python
"""
Lambda is an anonymous function, it accepts parameters but serve a single instruction without the keyword return without loops, just a simple instruction
"""

fn = lambda x : x ** 2
print(fn(5))
# Outputs : 25
```