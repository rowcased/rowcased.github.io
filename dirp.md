## Directory Print

This was helpful when was first learning data types.
Note: it contains a call to the [namer()](/namer) function.

```python
def dirp(name):

    ''' pretty prints the directory of an object '''
    
    head = __import__('toolbox').namer(name)
    lead = "\n dirp({}):\n\n  {}\n"
    directory = dir(name)
    
    print(lead.format(head, type(name))) 
    for i, item in enumerate(directory, 1):
        print("  {} {}".format(i, item))
    print()
    
    return directory
```



[back to toolkit](/toolkit_page)
