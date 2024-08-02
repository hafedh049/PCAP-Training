<span style="color:rgb(0, 176, 240)">O</span><span style="color:rgb(0, 176, 80)">O</span><span style="color:rgb(255, 0, 0)">P</span> stands for <span style="color:rgb(0, 176, 240)">O</span>bject <span style="color:rgb(0, 176, 80)">O</span>riented <span style="color:rgb(255, 0, 0)">P</span>rogramming

```python
class A:
	pass
```

Here we define a class named **A** that has nothing (Neither **attributes** nor **methods**)

```python
class A:
	def __init__(self, *args, **kwargs):
		self.args = args
		self.kwargs = kwargs
		print(f"args: {self.args}",f"kwargs: {self.kwargs}",sep="\n",end="\n")

obj_a = A(1,2,3,a=5,b=6)
```

This is the output:

![[Pasted image 20240801094530.png]]

So lets break the code part by part:

```python
def __init__(self, *args, **kwargs):
	...
```

This is called **constructor** and there are **2 types** of it **explicit** one and **implicit** one
the implicit constructor is created automatically and the other one need to be created using the ______init______ . The **self** argument need to be passed as the first parameter in the constructor, the self argument is a reference of the current object so we can later use it to access the object attributes like that **self.args** and **self.kwargs**