hi this is dirp

```python
def dirp(name): # well, uh... can
    #import inspect
    #head = inspect.stack()[1][-2][0][
    #       inspect.stack()[1][-2][0].index('(')+1:
    #       -(inspect.stack()[1][-2][0][::-1].index(')')+1)]
    
    import inspect
    inst = inspect.stack()[1][-2][0]      # gotta
    start = inst.index('(') + 1           # regex
    stop = -(inst[::-1].index(')') + 1)   # this!
    head = inst[start:stop]
    #return name
    
    #print(' dir('+name.__name__+'):')
    print('\n dirp('+head+'):\n\n ',type(name),'\n')
    for d,nom in enumerate(dir(name)):
        print(' ',d,nom)
    print()
    return dir(name)
```


[back to toolkit](/toolkit_page)
