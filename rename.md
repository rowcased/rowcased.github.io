## Variable Renamer

This function is part of a larger program. Its purpose was to rename a function in a "_raw.py" file that contained many dufferent solutions of the same function. These functions were later to be parsed fromm the raw file and then each run for time seperately.

<br>Note: it contains a call to the [namer()](/namer.md) function.

```python
def rename(old, new):
    
    '''   replaces occurances of a given
          name with a replacement name '''
    
    with open(new + '_raw.py','r',
        encoding = ('UTF-8')) as file:
            raw = file.read()
            
    raw = raw.replace(old, new)
    
    with open(new + '_raw.py','w',
        encoding = ('UTF-8')) as file:
            file.write(raw)
```



[back to toolkit](/toolkit_page)
