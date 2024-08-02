```python
import subprocess

# Basic usage of subprocess.run to execute a shell command
result = subprocess.run(
    ["echo", "Hello, World!"], capture_output=True, text=True, shell=True
)

# Print the results
print(f"Command: {' '.join(result.args)}")
print(f"Return Code: {result.returncode}")
print(f"Output: {result.stdout}")
print(f"Error: {result.stderr}")
print()

# Example with more complex command and error handling
command = ["type", "test.py"]
try:
    result = subprocess.run(
        command, capture_output=True, text=False, check=False, shell=True
    )

    print(f"Command: {' '.join(result.args)}")
    print(f"Return Code: {result.returncode}")
    print(f"Output: {result.stdout}")
    print(f"Error: {result.stderr}")
except subprocess.CalledProcessError as e:
    print(f"Command '{' '.join(e.cmd)}' failed with return code {e.returncode}")
    print(f"Output: {e.output}")
    print(f"Error: {e.stderr}")
print()

# Example of running a command and providing input
result = subprocess.run(
    ["python", "-c", "print(input())"],
    input="Hello, Python!",
    capture_output=True,
    text=True,
)

print(f"Command: {' '.join(result.args)}")
print(f"Return Code: {result.returncode}")
print(f"Output: {result.stdout}")
```