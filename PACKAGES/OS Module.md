```python
import os

# 1. Join one or more path components intelligently
path = os.path.join(".", "my_folder", "my_file.txt")
print(f"Joined Path: {path}")

# 2. Check if a path exists
file_exists = os.path.exists("file.txt")
print(f"Does 'file.txt' exist? {file_exists}")

# 3. Get the current working directory
cwd = os.getcwd()
print(f"Current Working Directory: {cwd}")

# 4. Run a shell command (returns the exit status)
exit_status = os.system("echo Hello, World!")
print(f"Exit Status of the command: {exit_status}")

# 5. Change the current working directory
os.chdir("..")
new_cwd = os.getcwd()
print(f"New Working Directory after chdir: {new_cwd}")

# 6. Close a file descriptor (requires a valid file descriptor)
# This is not typically used directly, instead, use file object methods.
fd = os.open("file.txt", os.O_RDWR)
os.close(fd)

# 7. List the contents of a directory
contents = os.listdir(".")
print(f"Contents of the current directory: {contents}")

# 8. Create a leaf directory and all intermediate ones
os.makedirs("new_dir/sub_dir", exist_ok=True)
print(f"Created 'new_dir/sub_dir'")

# 9. Create a directory
os.mkdir("another_dir")
print(f"Created 'another_dir'")

# 10. Remove (delete) a file
with open("delete_me.txt", "w") as f:
    f.write("This file will be deleted.")
os.remove("delete_me.txt")
print(f"Deleted 'delete_me.txt'")

# 11. Remove (delete) an empty directory
os.rmdir("another_dir")
print(f"Removed 'another_dir'")

# 12. Rename a file or directory
with open("rename_me.txt", "w") as f:
    f.write("This file will be renamed.")
os.rename("rename_me.txt", "renamed.txt")
print(f"Renamed 'rename_me.txt' to 'renamed.txt'")

# 13. Rename a file or directory, moving it to a different location if necessary
os.makedirs("dir1/dir2", exist_ok=True)
os.renames("renamed.txt", "dir1/dir2/moved_and_renamed.txt")
print(f"Renamed and moved 'renamed.txt' to 'dir1/dir2/moved_and_renamed.txt'")

# 14. Generate file names in a directory tree, walking top-down or bottom-up
for root, dirs, files in os.walk("."):
    print(f"Root: {root}")
    print(f"Directories: {dirs}")
    print(f"Files: {files}")
```

> [!important]
> **Explanation:**
> 1. `os.path.join(".")` combines directory and file names into a single path.
>2. `os.path.exists("file.txt")` checks if a file or directory exists.
>3. `os.getcwd()` returns the current working directory.
>4. `os.system("echo Hello, World!")` runs a shell command.
>5. `os.chdir("..")` changes the current working directory to the parent directory.
>6. `os.close(fd)` closes a file descriptor (typically handled by file objects).
>7. `os.listdir(".")` lists the contents of the specified directory.
>8. `os.makedirs("new_dir/sub_dir", exist_ok=True)` creates directories, including intermediate directories.
>9. `os.mkdir("another_dir")` creates a single directory.
>10. `os.remove("delete_me.txt")` deletes a file.
>11. `os.rmdir("another_dir")` removes an empty directory.
>12. `os.rename("rename_me.txt", "renamed.txt")` renames a file or directory.
>13. `os.renames("renamed.txt", "dir1/dir2/moved_and_renamed.txt")` renames and possibly moves a file or directory.
>14. `os.walk(".")` generates file names in a directory tree.
