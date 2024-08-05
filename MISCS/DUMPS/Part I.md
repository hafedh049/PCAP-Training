
> [!important]
> ### Question 1
> What is true about Python packages? (Choose two.)
> - **A.** a code designed to initialize a package’s state should be placed inside a file named init.py
> - **B.** a package’s contents can be stored and distributed as an mp3 file
> - **C.** __pycache__ is a folder that stores semi-compiled Python modules
> - **D.** the sys.path variable is a list of strings
>  >[!note]- Responses
>  >- A $\color{green}\checkmark$
>  >- D $\color{green}\checkmark$
>  

Got it! Here's the corrected format with the responses belonging to the `Responses` collapsible section:

> [!important]
> ### Question 2 ( Exam A )
> What is the expected output of the following code?
> ```python
> import sys
> import math
> b1 = type(dir(math)) is list
> b2 = type(sys.path) is list
> print(b1 and b2)
> ```
> - **A.** None
> - **B.** True
> - **C.** 0
> - **D.** False
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$

> [!important]
> ### Question 3 ( Exam A )
> A Python package named pypack includes a module named pymod.py which contains a function named pyfun().
> Which of the following snippets will let you invoke the function? (Choose two.)
> 
> - **A.** `from pypack.pymod import pyfun`
>   `pyfun()`
> - **B.** `import pypack`
>   `pymod.pyfun()`
> - **C.** `from pypack import *`
>   `pyfun()`
> - **D.** `import pypack`
>   `import pypack.pymod`
>   `pypack.pymod.pyfun()`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- D $\color{green}\checkmark$

> [!important]
> ### Question 4 ( Exam A )
> Assuming that the code below has been executed successfully, which of the following expressions will always evaluate to True? (Choose two.)
> ```python
> import random
> v1 = random.random()
> v2 = random.random()
> ```
> - **A.** `len(random.sample([1,2,3],1)) > 2`
> - **B.** `v1 == v2`
> - **C.** `random.choice([1,2,3]) > 0`
> - **D.** `v1 < 1`
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- D $\color{green}\checkmark$

> [!important]
> ### Question 5 ( Exam A )
> With regards to the directory structure below, select the proper forms of the directives in order to import module_c. (Choose two.)
> ```css
> pypack (dir)
> ├── upper (dir)
> │   ├── lower (dir)
> │   │   └── module_c.py (file)
> │   └── module_b.py (file)
> └── module_a.py (file)
> ```
> - **A.** `from pypack.upper.lower import module_c`
> - **B.** `import pypack.upper.lower.module_c`
> - **C.** `import upper.module_c`
> - **D.** `import upper.lower.module_c`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$

> [!important]
> ### Question 6 ( Exam A )
> Which one of the platform module functions should be used to determine the underlying platform name?
> 
> - **A.** `platform.processor()`
> - **B.** `platform.uname()`
> - **C.** `platform.python_version()`
> - **D.** `platform.platform()`
> 
> >[!note]- Responses
> >- D $\color{green}\checkmark$

Here’s the formatted question using your template:

> [!important]
> ### Question 7 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> S = '2A'
> try:
>    n = int(s)
> except ValueError:
>    n = 2
> except ArithmeticError:
>    n = 1
> except:
>    n = 0
> print (n)
> ```
> 
> - **A.** the code is erroneous and it will not execute
> - **B.** it outputs 1
> - **C.** it outputs 2
> - **D.** it outputs 0
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 8 ( Exam A )
> Which of the following snippets will execute without raising any unhandled exceptions? (Choose two.)
> 
> - **A.**
> ```python
> try:
>    print(-1/1)
> except:
>    print(0/1)
> else:
>    print(1/1)
> ```
> - **B.**
> ```python
> try:
>    X = 1
> except:
>    X = X + 1
> else:
>    X = X + 2
> ```
> - **C.**
> ```python
> try:
>    x = y + 1
> except (NameError, SystemError):
>    x = y + 1
> else:
>    y = x
> ```
> - **D.**
> ```python
> try:
>    X = 1 / 0
> except NameError:
>    x = 1 / 1
> else:
>    X = X + 1
> ```
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 9 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> m = 0
> 
> def foo (n): 
> 	global m
> 	assert m == 0
> 	try:
> 	   return 1/n
> 	except ArithmeticError:
> 	   m += 1
> 	   raise
> 	   
> try:
>    foo (0)
> except ArithmeticError:
>    m + 2
> except:
>    m += 1
>    
> print (m)
> ```
> 
> - **A.** it outputs 3
> - **B.** it outputs 1
> - **C.** it outputs 2
> - **D.** the code is erroneous and it will not execute
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 10 ( Exam A )
> What is true about the following snippet? (Choose two.)
> 
> ```python
> class E(Exception):
>    def __init__(self, message):
>        self.message = message
>    def __str__(self):
>        return "it's nice to see you"
> try:
>    print("I feel fine")
>    raise E("what a pity")
> except E as e:
>    print(e)
> else:
>    print("the show must go on")
> ```
> 
> - **A.** the string what a pity will be seen
> - **B.** the string it's nice to see you will be seen
> - **C.** the code will raise an unhandled exception
> - **D.** the string I feel fine will be seen
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 11 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> my_list = [1, 2, 3]
> try:
>    my_list[3] = my_list[2]
> except BaseException as error:
>    print(error)
> ```
> 
> - **A.** it outputs error
> - **B.** it outputs
> - **C.** the code is erroneous and it will not execute
> - **D.** it outputs list assignment index out of range
> 
> >[!note]- Responses
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 12 ( Exam A )
> Which of the following expressions evaluate to True? (Choose two.)
> 
> - **A.** `ord("0") - ord("9") == 10`
> - **B.** `len("''") == 2`
> - **C.** `chr(ord('z') - 1) == 'y'`
> - **D.** `len(''1234'') == 4`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 13 ( Exam A )
> Which of the following expressions evaluate to True? (Choose two.)
> 
> - **A.** `'xYz'.lower() > 'XY'`
> - **B.** `'8' + '8' != 2 * '8'`
> - **C.** `float('3.14') == str('3.' + '14')`
> - **D.** `121 + 1 == int('1' + 2 * '2')`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 14 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> string = str(1/3)
> dummy = ""
> for character in string:
>    dummy = dummy + character
> print(dummy[-1])
> ```
> 
> - **A.** it outputs 3
> - **B.** it outputs 'None'
> - **C.** it outputs 0
> - **D.** it raises an exception
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 15 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> the_list = "alpha;beta;gamma".split(";")
> the_string = ''.join(the_list)
> print(the_string.isalpha())
> ```
> 
> - **A.** it outputs True
> - **B.** it outputs False
> - **C.** it outputs nothing
> - **D.** it raises an exception
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 16 ( Exam A )
> Which of the following invocations are valid? (Choose two.)
> 
> - **A.** `sort("python")`
> - **B.** `"python".find("")`
> - **C.** `"python".sort()`
> - **D.** `sorted("python")`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 17 ( Exam A )
> Which of the following expressions evaluate to True? (Choose two.)
> 
> - **A.** `'in' in 'in'`
> - **B.** `'in' in 'Thames'`
> - **C.** `'in not' in 'not'`
> - **D.** `'t'.upper() in 'Thames'`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 18 ( Exam A )
> Assuming that the snippet below has been executed successfully, which of the following expressions will evaluate to True? (Choose two.)
> 
> ```python
> string = 'python'[::2]
> string = string[-1] + string[-2]
> ```
> 
> - **A.** `len(string) == 3`
> - **B.** `string[0] == 'o'`
> - **C.** `string[0] == string[-1]`
> - **D.** `string is None`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 19 ( Exam A )
> Which of the following statements are true? (Choose two.)
> 
> - **A.** an escape sequence can be recognized by the `/` sign put in front of it
> - **B.** ASCII is a subset of UNICODE
> - **C.** II in ASCII stands for Internal Information
> - **D.** a code point is a number assigned to a given character
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 20 ( Exam A )
> A property that stores information about a given class’s super-classes is named:
> 
> - **A.** `__bases__`
> - **B.** `__super__`
> - **C.** `__upper__`
> - **D.** `__ancestors__`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 21 ( Exam A )
> Assuming that the code below has been executed successfully, which of the following expressions evaluate to True? (Choose two.)
> 
> ```python
> class Class:
>    var data
>    def __init__(self, value):
>        self.prop = value
> Object = Class(2)
> ```
> 
> - **A.** `'var' in Class.__dict__`
> - **B.** `'data' in Object.__dict__`
> - **C.** `len(Class.__dict__) == 1`
> - **D.** `'data' in Class.__dict__`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 22 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> class Super:
>    def make(self):
>        return 0
>    def doit(self):
>        return self.make()
> class SubA(Super):
>    def make(self):
>        return 1
> class SubB(Super):
>    pass
> a = SubA()
> b = SubB()
> print(a.doit() + b.doit())
> ```
> 
> - **A.** it outputs 1
> - **B.** it outputs 0
> - **C.** it raises an exception
> - **D.** it outputs 2
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 23 ( Exam A )
> Assuming that the code below has been placed inside a file named `code.py` and executed successfully, which of the following expressions evaluate to True? (Choose two.)
> 
> ```python
> class ClassA:
>    var = 1
>    def __init__(self, prop):
>        prop1 = prop2 = prop
> class ClassB(ClassA):
>    def __init__(self, prop):
>        self.prop3 = prop ** 2
>        super().__init__(prop)
> Object = ClassB(2)
> ```
> 
> - **A.** `str(Object) == 'Object'`
> - **B.** `__name__ == '__main__'`
> - **C.** `len(ClassB.__bases__) == 1`
> - **D.** `ClassA.__module__ == 'ClassA'`
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 24 ( Exam A )
> Assuming that the following inheritance set is in force, which of the following classes are declared properly? (Choose two.)
> 
> ```python
> class A:
>    pass
> class B(A):
>    pass
> class C(A):
>    pass
> ```
> 
> - **A.** `class Class_3(A, C): pass`
> - **B.** `class Class_2(B, C): pass`
> - **C.** `class Class_4(A, B): pass`
> - **D.** `class Class_1(C, B): pass`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 25 ( Exam A )
> Assuming that the following piece of code has been executed successfully, which of the expressions evaluate to True? (Choose two.)
> 
> ```python
> class A:
>    VarA = 1
>    def __init__(self):
>        self.prop_a = 1
> class B(A):
>    VarA = 2
>    def __init__(self):
>        super().__init__()
>        self.prop_b = 2
> obj_a = A()
> obj_aa = A()
> obj_b = B()
> obj_bb = B()
> ```
> 
> - **A.** `A.VarA == 1`
> - **B.** `isinstance(obj_b, A)`
> - **C.** `B.VarA == 1`
> - **D.** `obj_a is obj_aa`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 26 ( Exam A )
> What is the expected output of the following snippet?
> 
> ```python
> class Upper:
>    def __init__(self):
>        self.property = 'upper'
> class Lower(Upper):
>    def __init__(self):
>        super().__init__()
> Object = Lower()
> print(isinstance(Object, Lower), end=' ')
> print(Object.property)
> ```
> 
> - **A.** `False upper`
> - **B.** `True upper`
> - **C.** `False lower`
> - **D.** `True lower`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 27 ( Exam A )
> Which of the following lines of code will work flawlessly when put independently inside the `dup()` method in order to make the snippet’s output equal to `[0, 1, 1]`? (Choose two.)
> 
> ```python
> class MyClass:
>    def __init__(self, initial):
>        self.store = initial
>    def put(self, new):
>        self.store.append(new)
>    def get(self):
>        return self.store
>    def dup(self):
>        # insert the line of code here
> Object = MyClass([0])
> Object.put(1)
> Object.dup()
> print(Object.get())
> ```
> 
> - **A.** `self.put(self.store[1])`
> - **B.** `self.put(self.get()[-1])`
> - **C.** `self.put(store[1])`
> - **D.** `put(self.store[1])`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 28 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> class Class:
>    Variable = 0
>    def __init__(self):
>        self.value = 0
> object_1 = Class()
> Class.Variable += 1
> object_2 = Class()
> object_2.value += 1
> print(object_2.Variable + object_1.value)
> ```
> 
> - **A.** it raises an exception
> - **B.** it outputs 2
> - **C.** it outputs 0
> - **D.** it outputs 1
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 29 ( Exam A )
> What is true about Object-Oriented Programming in Python? (Choose two.)
> 
> - **A.** encapsulation allows you to hide a whole class inside a package
> - **B.** a class is a recipe for an object
> - **C.** each object of the same class can have a different set of properties
> - **D.** the arrows on a class diagram are always directed from a superclass towards its subclass
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 30 ( Exam A )
> What is true about Python class constructors? (Choose two.)
> 
> - **A.** the constructor’s first parameter identifies an object currently being created
> - **B.** super-class constructor is invoked implicitly during constructor execution
> - **C.** the constructor can be invoked directly under strictly defined circumstances
> - **D.** the constructor cannot use the default values of the parameters
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 31 ( Exam A )
> Which of the following lambda function definitions are correct? (Select two answers)
> 
> - **A.** `lambda X: None`
> - **B.** `lambda: 3,1415`
> - **C.** `lambda x: def fun(x): return x`
> - **D.** `lambda lambda: lambda * lambda`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 32 ( Exam A )
> Which of the following expressions evaluate to True? (Select two answers)
> 
> - **A.** `'in not' in 'not'`
> - **B.** `'in' in 'Thames'`
> - **C.** `'t'.upper() in 'Thames'`
> - **D.** `'in' in 'in'`
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- D $\color{green}\checkmark$

Here’s the formatted question:

> [!important]
> ### Question 33 ( Exam A )
> Which of the following snippets will execute without raising any unhandled exceptions? (Select answers)
> 
> - **A.**
> 
> ```python
> try:
>    print(int("0"))
> except NameError:
>    print("0")
> else:
>    print(int(""))
> ```
> 
> - **B.**
> 
> ```python
> try:
>    print(0/0)
> except:
>    print(0/1)
> else:
>    print(0/2)
> ```
> 
> - **C.**
> 
> ```python
> import math
> try:
>    print(math.sqrt(-1))
> except:
>    print(math.sqrt(0))
> else:
>    print(math.sqrt(1))
> ```
> 
> - **D.**
> 
> ```python
> try:
>    print(float("le1"))
> except (NameError, SystemError):
>    print(float("1a1"))
> else:
>    print(float("1c1"))
> ```
> 
> >[!note]- Responses
> >- C $\color{red}\checkmark$
> >
> 

Here’s the formatted question:

> [!important]
> ### Question 34 ( Exam A )
> Which of the following invocations are valid? (Select two answers)
> 
> - **A.** `rfind("python","r")`
> - **B.** `sorted("python")`
> - **C.** `"python".sort()`
> - **D.** `"python".index("th")`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 35 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> class Class:
>    _Var = 1
>    __Var = 2
>    def __init__(self):
>        self._prop = 3
>        self.__prop = 4
> o = Class()
> print(o._Class__Var + o._Class__prop)
> ```
> 
> - **A.** it outputs 6
> - **B.** it outputs 1
> - **C.** it outputs 3
> - **D.** it raises an exception
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 36 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> x = 8 ** (1/3)
> y = 2. if x < 2.3 else 3.0
> print(y)
> ```
> 
> - **A.** it outputs 2.0
> - **B.** it outputs 2.5
> - **C.** the code is erroneous and it will not execute
> - **D.** it outputs 3.0
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 37 ( Exam A )
> What is the expected output of the following code if the file named `zero_length_existing_file` is a zero-length file located inside the working directory?
> 
> ```python
> try:
>    f = open('zero_length_existing_file', 'rt')
>    d = f.readline()
>    print(len(d))
>    f.close()
> except IOError:
>    print(-1)
> ```
> 
> - **A.** 0
> - **B.** -1
> - **C.** an errno value corresponding to file not found
> - **D.** 2
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 38 ( Exam A )
> What is true about Python class constructors? (Select two answers)
> 
> - **A.** the constructor must have at least one parameter
> - **B.** the constructor must return a value other than None
> - **C.** the constructor is a method named `__init__`
> - **D.** there can be more than one constructor in a Python class
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- A $\color{red}\checkmark$


> [!important]
> ### Question 39 ( Exam A )
> What is the expected output of the following code?
> 
> ```python
> def foo(x, y, z):
>    return x(y) - x(z)
> 
> print(foo(lambda x: x % 2, 2, 1))
> ```
> 
> - **A.** 1
> - **B.** 0
> - **C.** -1
> - **D.** an exception is raised
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 40 ( Exam A )
> Which of the listed actions can be applied to the following tuple? (Select two answers)
> 
> - **A.** `tup[:]`
> - **B.** `tup.append(0)`
> - **C.** `tup[0]`
> - **D.** `del tup`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- C $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 41 ( Exam A )
> There is a stream named `s` open for writing. 
> 
> What option will you select to write a line to the stream?
> 
> - **A.** `s.write("Hello\n")`
> - **B.** `write(s, "Hello")`
> - **C.** `s.writeln("Hello")`
> - **D.** `s.writeline("Hello")`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 42 ( Exam A )
> What is the expected output of the following code if `existing_file` is the name of a file located inside the working directory?
> 
> ```python
> try:
>    f = open('existing_file', 'w')
>    print(1, end=' ')
> except IOError as error:
>    print(error.errno, end=' ')
>    print(2, end=' ')
> else:
>    f.close()
>    print(3, end=' ')
> ```
> 
> - **A.** 1 2
> - **B.** 1 2 3
> - **C.** 1 3
> - **D.** 2 3
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 43 ( Exam A )
> Files with the suffix `.pyc` contain:
> 
> - **A.** Python source code
> - **B.** backups
> - **C.** temporary data
> - **D.** semi-compiled Python code
> 
> >[!note]- Responses
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 44 ( Exam A )
> What is true about Python packages? (Select two answers)
> 
> - **A.** the `sys.path` variable is a list of strings
> - **B.** `_pycache_` is a folder that stores semi-compiled Python modules
> - **C.** a package's contents can be stored and distributed as an mp3 file
> - **D.** code designed to initialize a package's state should be placed inside a file named `__init__.py`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 45 ( Exam A )
> Which of the following statements are true? (Select two answers)
> 
> - **A.** `e` is an escape sequence used to mark the end of lines
> - **B.** ASCII is synonymous with UTF-8
> - **C.** II in ASCII stands for Information Interchange
> - **D.** a code point is a number assigned to a given character
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 46 ( Exam A )
> What is the expected output of the following snippet?
> 
> ```python
> a = 2
> if a > 0:
>    a += 1
> else:
>    a -= 1
> print(a)
> ```
> 
> - **A.** 3
> - **B.** 1
> - **C.** 2
> - **D.** the code is erroneous
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 47 ( Exam A )
> Which of the following lambda definitions are correct? (Select two answers)
> 
> - **A.** `lambda x, y: x // y - x % y`
> - **B.** `lambda x, y; x // y - x % y`
> - **C.** `lambda x, y = x // y, x % y`
> - **D.** `lambda x, y: (x, y)`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 48 ( Exam A )
> If you need a function that does nothing, what would you use instead of `XXX`? (Select four answers)
> 
> ```python
> def idler():
>    XXX
> ```
> 
> - **A.** `pass`
> - **B.** `return`
> - **C.** `exit`
> - **D.** `None`
> - **E.** `...`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$
> >- E $\color{green}\checkmark$


> [!important]
> ### Question 49 ( Exam A )
> A file name like this one below says mat: (select three answers)
> 
> `services.cpython-36.pyc`
> 
> - **A.** the interpreter used to generate the file is version 3.6
> - **B.** it has been produced by CPython
> - **C.** it is the 36th version of the file
> - **D.** the file comes from the `services.py` source file
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 50 ( Exam A )
> What is the expected behavior of the following code?
> 
> ```python
> my_list = [i for i in range(5, 0, -1)]
> m = [my_list[i] for i in range(5) if my_list[i] % 2 == 0]
> print(m)
> ```
> 
> - **A.** the code is erroneous and it will not execute
> - **B.** it outputs [2, 4]
> - **C.** it outputs [4, 2]
> - **D.** it outputs [0, 1, 2, 3, 4]
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$

