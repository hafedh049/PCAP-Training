
> [!important]
> ### Question 51 ( Exam A )
> Assuming that the snippet below has been executed successfully, which of the following expressions will evaluate to True? (Select two answers)
> 
> ```python
> string = 'python'[::2]
> string = string[-1] + string[-2]
> ```
> 
> - **A.** `string[0] == string[-1]`
> - **B.** `string is None`
> - **C.** `len(string) == 3`
> - **D.** `string[0] == 'o'`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 52 ( Exam A )
> The following class definition is given:
> 
> ```python
> class Class:
>     def __init__(self, val):
>         self.val = val
>     
>     def get(self):
>         return self.val
>     
>     def show(self):
>         XXX
> ```
> 
> We want the `show()` method to invoke the `get()` method, and then output the value the `get()` method returns.
> 
> Which of the invocations should be used instead of `XXX`?
> 
> - **A.** `print(get(self))`
> - **B.** `print(self.get())`
> - **C.** `print(get())`
> - **D.** `print(self.get(val))`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$

Here’s the formatted question:

> [!important]
> ### Question 53 ( Exam A )
> A property that stores information about a given class's super-classes is named:
> 
> - **A.** `__upper__`
> - **B.** `__bases__`
> - **C.** `__ancestors__`
> - **D.** `__super__`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 54 ( Exam A )
> The simplest possible class definition in Python can be expressed as:
> 
> - **A.** `class X:`
> - **B.** `class X: pass`
> - **C.** `class X: return`
> - **D.** `class X: {}`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 55 ( Exam A )
> Assuming that the following piece of code has been executed successfully, which of the expressions evaluate to True? (Select two answers)
> 
> ```python
> class A:
>     VarA = 1
>     def __init__(self):
>         self.prop_a = 1
> 
> class B(A):
>     VarA = 2
>     def __init__(self):
>         self.prop_a = 2
>         self.prop_aa = 2
> 
> class C(B):
>     VarA = 3
>     def __init__(self):
>         super().__init__()
> 
> obj_a = A()
> obj_b = B()
> obj_c = C()
> ```
> 
> Which of the following expressions evaluate to True? (Select two answers)
> 
> - **A.** `obj_b.prop_a == 3`
> - **B.** `hasattr(obj_b, 'prop_aa')`
> - **C.** `isinstance(obj_c, A)`
> - **D.** `VarA == 3`
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$
> >- B $\color{green}\checkmark$


> [!important]
> ### Question 56 ( Exam A )
> Which of the following statements are true? (Select two answers)
> 
> - **A.** `open()` requires a second argument
> - **B.** `open()` is a function which returns an object that represents a physical file
> - **C.** `stdin`, `stdout`, `stderr` are the names of pre-opened streams
> - **D.** If invoking `open()` fails, an exception is raised
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 57 ( Exam A )
> Which line can be used instead of the comment to cause the snippet to produce the following expected output? (Select two answers)
> 
> **Expected output:**
> ```
> 1 2 3
> ```
> 
> **Code:**
> ```python
> c, b, a = 1, 3, 2 
> # put line here
> print(a, b, c)
> ```
> 
> - **A.** `c, b, a = b, a, c`
> - **B.** `c, b, a = a, c, b`
> - **C.** `a, b, c = c, a, b`
> - **D.** `a, b, c = a, b, c`
> 
> >[!note]- Responses
> >- B $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 58 ( Exam A )
> How many elements will the `list1` list contain after execution of the following snippet?
> 
> **Code:**
> ```python
> list1 = ['zero', 'one']
> list1.insert(1, 'two')
> list1.append('three')
> ```
> 
> - **A.** two
> - **B.** zero
> - **C.** one
> - **D.** three
> - **E.** four
> 
> >[!note]- Responses
> >- E $\color{green}\checkmark$


> [!important]
> ### Question 59 ( Exam A )
> What is the expected output of the following code?
> 
> **Code:**
> ```python
> class A:
>     def a(self):
>         print("A", end='')
>     def b(self):
>         self.a()
> 
> class B(A):
>     def a(self):
>         print("B", end='')
>     def do(self):
>         self.b()
> 
> class C(A):
>     def a(self):
>         print("C", end='')
>     def do(self):
>         self.b()
> 
> B().do()
> C().do()
> ```
> 
> - **A.** BB
> - **B.** CC
> - **C.** AA
> - **D.** BC
> 
> >[!note]- Responses
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 60 ( Exam A )
> Assuming that the following snippet has been successfully executed, which of the equations are True? (Select two answers)
> 
> **Code:**
> ```python
> a = [1]
> b = a
> a[0] = 0
> ```
> 
> - **A.** `len(a) == len(b)`
> - **B.** `b[0] == 1 == a[0]`
> - **C.** `a[0] == b[0]`
> - **D.** `a[0] + 1 == b[0]`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 61 ( Exam A )
> A method for passing the arguments used by the following snippet is called:
> 
> ```python
> def fun(a, b, *args, **kwargs, c = None):
>     return a + b
> 
> res = fun(1, 2)
> ```
> 
> - **A.** sequential
> - **B.** named
> - **C.** positional
> - **D.** keyword
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 62 ( Exam A )
> What is the output of the following code?
> 
> ```python
> def f(*args, **kwargs):
>     print(args, kwargs)
> 
> print(f(1, 2, 3,));
> ```
> 
> - **A.** The code is erroneous
> - **B.** (1, 2, 3) {}
> - **C.** (1, 2, 3) {}\nNone
> - **D.** The reference of the callback in memory
> 
> >[!note]- Responses
> >- C $\color{green}\checkmark$


> [!important]
> ### Question 63 ( Exam A )
> What is the output of the following code?
> 
> ```python
> def f(x, *args, *kwargs, k=None):
>   ...
> 
> print(f(None,None,None));;
> ```
> 
> - **A.** The code is erroneous
> - **B.** None
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 64 ( Exam A )
> How many lines does the following snippet output?
> 
> ```python
> for i in range(1, 3): 
>   print("*", end="")
> else:
>   print("*")
> ```
> 
> - **A.** three
> - **B.** one
> - **C.** two
> - **D.** four
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$


> [!important]
> ### Question 65 ( Exam A )
> What will the value of the `i` variable be when the following loop finishes its execution?
> 
> ```python
> for i in range(10):
>     pass
> ```
> 
> - **A.** 10
> - **B.** the variable becomes unavailable
> - **C.** 11
> - **D.** 9
> 
> >[!note]- Responses
> >- D $\color{green}\checkmark$


> [!important]
> ### Question 66 ( Exam A )
> Which of the following literals reflect the value given as `34.23`? (Select two answers)
> 
> - **A.** `.3423e2`
> - **B.** `3423e-2`
> - **C.** `.3423e-2`
> - **D.** `3423e2`
> 
> >[!note]- Responses
> >- A $\color{green}\checkmark$
> >- B $\color{green}\checkmark$

