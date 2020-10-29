## Variable Name Getter

This program is used by several other tools in my toolkit such as:<br>
[rename()](/rename.md), [dirp()](/dirp.md), and [qsp()](/qsp.md).

```python
def namer(object):

    ''' returns a string of the name of any object'''
    
    inst = __import__('inspect').stack()[1][-2][0]
    start = inst.index('(') + 1
    stop = -(inst[::-1].index(')') + 1)
    name = inst[start:stop]
    
    return name
```


[back to toolkit](/toolkit)
