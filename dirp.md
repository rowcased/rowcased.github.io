hi this is dirp

```python
#from toolbox import namer

def dirp(name):

    ''' pretty prints the directory of an object '''
    
    head = __import__('toolbox').namer(name)
    
    #print('\n dirp(' + head + '):\n\n ',type(name),'\n')
    print("\n dirp({}):\n\n  {}\n".format(head, type(name)))
    
    for d, nom in enumerate(dir(name)):
        #print(' ', d, nom)
        print("  {} {}".format(d, nom))
    print()
    
    return dir(name)
```



[back to toolkit](/toolkit_page)
