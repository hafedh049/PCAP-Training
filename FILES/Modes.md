### Reading Modes

1. **`r` (Read) or `rt` :**
    
    - Opens the file for reading only.
    - The file must exist; otherwise, an error is raised.

```python
with open('file.txt', 'r') as file:     
	  	  content = file.read()
	  	  print(content)
```

### Writing Modes

2. **`w` (Write) or `wt` :
    
    - Opens the file for writing only.
    - If the file exists, it truncates (overwrites) the file.
    - If the file does not exist, it creates a new file.
    
```python
with open('file.txt', 'w') as file:     
	file.write('Hello, World!')
```
### Appending Modes

3. **`a` (Append) or `at` :**
    
    - Opens the file for writing only.
    - If the file exists, the file pointer is at the end of the file. The file is not truncated.
    - If the file does not exist, it creates a new file.

```python
with open('file.txt', 'a') as file:     
	file.write('Hello, World!')
```

### Mix Modes

4. **`r+` (Read and Write) or `r+t`:**
    
    - Opens the file for both reading and writing.
    - The file must exist; otherwise, an error is raised.
    - The file pointer is at the beginning of the file.
    
```python
with open('file.txt', 'r+') as file:     
    content = file.read()     
    file.write('Hello, World!')
```
	
1. **`w+` (Write and Read) or `w+t`:**
    
    - Opens the file for both writing and reading.
    - If the file exists, it truncates the file.
    - If the file does not exist, it creates a new file.
    - The file pointer is at the beginning of the file.
    
 ```python
with open('file.txt', 'w+') as file:     
	file.write('Hello, World!')
	file.seek(0)
	content = file.read()
```
    
6. **`a+` (Append and Read) or `a+t`:**
    
    - Opens the file for both writing and reading.
    - If the file exists, the file pointer is at the end of the file. The file is not truncated.
    - If the file does not exist, it creates a new file.

```python
with open('file.txt', 'a+') as file:
	file.write('Hello, World!')     
	file.seek(0)
	content = file.read()
# write(x) replace the current line by x 
```
### Binary Modes

Each of the above modes can be combined with `b` to operate in binary mode. This is useful for non-text files like images, videos, etc.

7. **Binary Read (`rb`):**
    
    - Opens the file for reading in binary mode.
    
```python
with open('file.txt', 'rb') as file:     
	content = file.read()
```
    
8. **Binary Write (`wb`):**
    
    - Opens the file for writing in binary mode.
    
```python
with open('file.txt', 'wb') as file:
	file.write(b'Hello, World!')
```
    
9. **Binary Append (`ab`):**
    
    - Opens the file for appending in binary mode.
    
```python
with open('file.txt', 'ab') as file:
	file.write(b'Hello, World!')
```
    
10. **Binary Read and Write (`r+b`):**
    
    - Opens the file for both reading and writing in binary mode.
    
    ```python
with open('file.txt', 'r+b') as file:
	content = file.read()
	file.write(b'Hello, World!')
```
    
11. **Binary Write and Read (`w+b`):**
    
    - Opens the file for both writing and reading in binary mode.
    
    ```python
with open('file.txt', 'w+b') as file:     
	file.write(b'Hello, World!')     
	file.seek(0)     
	content = file.read()
```
    
12. **Binary Append and Read (`a+b`):**
    
    - Opens the file for both appending and reading in binary mode.

```python
with open('file.txt', 'a+b') as file:
	file.write(b'Hello, World!')
	file.seek(0)     
	content = file.read()
```