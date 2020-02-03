hi this is dirp

```python
from toobox import namer

def dirp(name):

    ''' pretty prints a directory list of an object '''
    
    head = namer(name)
    
    print('\n dirp('+head+'):\n\n ',type(name),'\n')
    for d,nom in enumerate(dir(name)):
        print(' ',d,nom)
    print()
    
    return dir(name)
```



[back to toolkit](/toolkit_page)
