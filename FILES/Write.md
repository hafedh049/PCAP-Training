```python
"Suppose that the file exists and it contains 10 lines"
fp = open("pcap.txt","w") # or 'a'
print(fp.write("Salamou alaykom")) # replace the current line with that string
fp.seek(0)
print(fp.read(5)) # reads the first 5 characters (bytes)
#--------------------------------------------------------------------------
fp.seek(0)
print(fp.writelines(["line1\n","line2\n"])) # replace the current line with 
fp.close()
```

> [! important]
> Always remember the file pointer
