hi this is dirp

```python
def dirp(name): # well, shit. can
    import inspect
    head = inspect.stack()[1][-2][0][
           inspect.stack()[1][-2][0].index('(')+1:
           -(inspect.stack()[1][-2][0][::-1].index(')')+1)]
    #print(' dir('+name.__name__+'):')
    print('\n dirp('+head+'):\n\n ',type(name),'\n')
    for d,nom in enumerate(dir(name)):
        print(' ',d,nom)
    print()
    return dir(name)
```


[back to toolkit](/toolkit_page)
