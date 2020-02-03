## Variable Name Getter

This program gets put to use by several other tools
in my toolbox. For example, see [dirp()](/dirp.md).

```python
def namer(object):

    ''' returns a string of the name of any object'''
    
    import inspect
    
    inst = inspect.stack()[1][-2][0]      # gotta
    start = inst.index('(') + 1           # regex
    stop = -(inst[::-1].index(')') + 1)   # this!
    name = inst[start:stop]
    
    return name
```


[back to toolkit](/toolkit_page)
