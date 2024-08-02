```python
import sys

# 1. sys.path: List of directories that the interpreter will search for modules
print(f"sys.path: {sys.path}")

# 2. sys.argv: List of command line arguments passed to the script
print(f"sys.argv: {sys.argv}")

# 3. sys.getrecursionlimit: Get the maximum depth of the Python interpreter stack
recursion_limit = sys.getrecursionlimit()
print(f"Current recursion limit: {recursion_limit}")

# 4. sys.setrecursionlimit: Set the maximum depth of the Python interpreter stack
new_limit = 1500
sys.setrecursionlimit(new_limit)
print(f"New recursion limit set to: {new_limit}")

# 5. sys.exit: Exit from Python
sys.exit("Exiting the script")

# 6. exit: Exit the script (an alias for sys.exit)
exit("Exiting the script using exit()")

# 7. quit: Exit the script (an alias for sys.exit)
quit("Exiting the script using quit()")

# 8. sys.getrefcount: Return the reference count of an object
obj = []
print(f"Reference count of the object (list): {sys.getrefcount(obj)}")

def check_reference_count(obj):
    print(f"Reference count for object: {sys.getrefcount(obj)}")

sample_list = [1, 2, 3]
obj = sample_list
check_reference_count(obj)

# 9. sys.getsizeof: Return the size of an object in bytes
size_of_obj = sys.getsizeof(obj)
print(f"Size of the object (list) in bytes: {size_of_obj}")

# 10. Using sys.path to add a custom directory to the module search path
custom_path = "/path/to/my/modules"
if custom_path not in sys.path:
    sys.path.append(custom_path)
    print(f"Added custom path to sys.path: {custom_path}")

# 11. Using sys.argv to handle command line arguments
if len(sys.argv) > 1:
    script_name = sys.argv[0]
    first_arg = sys.argv[1]
    print(f"Script name: {script_name}")
    print(f"First argument: {first_arg}")

# 12. Using sys.getrecursionlimit and sys.setrecursionlimit to prevent RecursionError
def recursive_function(n):
    if n > 0:
        return recursive_function(n - 1)
    return n

try:
    print(recursive_function(1000))
except RecursionError as e:
    print(f"RecursionError: {e}")

# 13. Using sys.getsizeof to estimate memory usage
class MyClass:
    def __init__(self):
        self.data = [i for i in range(1000)]

instance = MyClass()
print(f"Size of MyClass instance: {sys.getsizeof(instance)} bytes")

# Note: sys.exit(), exit(), and quit() terminate the script and are usually used for error handling or user-initiated termination.
```

![[Pasted image 20240802095639.png]]