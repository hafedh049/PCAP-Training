```python
"Suppose that the file exists and it contains 10 lines"
fp = open("pcap.txt","r")
print(fp.read()) # same as .read(-1) which means all bytes
fp.seek(0)
print(fp.read(5)) # reads the first 5 characters (bytes)
#--------------------------------------------------------------------------
fp.seek(0)
print(fp.readline()) #same as .readline(-1)
fp.seek(0)
print(fp.readline(5)) # Reads the first 5 bytes of the current line
#--------------------------------------------------------------------------
fp.seek(0)
print(fp.readlines()) #same as .readlines(-1)
# It returns a list of lines as ['line1\n', ...]
fp.close()
```