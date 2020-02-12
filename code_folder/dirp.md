## Directory Print

This was helpful when was first learning data types.
<br>Note: it contains a call to the [namer()](/code_folder/namer.md) function.

```python
def dirp(object):

    ''' pretty prints the directory of an object '''
    
    head = __import__('toolbox').namer(object)
    lead = "\n dirp({}):\n\n  {}\n"
    directory = dir(object)
    
    print(lead.format(head, type(object))) 
    for i, item in enumerate(directory, 1):
        print("  {} {}".format(i, item))
    print()
    
    return directory
```



[back to toolkit](/toolkit)
