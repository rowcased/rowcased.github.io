## Variable Name Getter

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
