### Timer!

```python
def timer(function, args=None, reps=1, show=True):

<!--    # <-- write declaration to compare multiple of same  -->
    
    ''' returns (optionally prints) execution time
        of a program based on given input and reps '''
    
    from time import time
    
    duration = 0
    
    for rep in range(reps):
        start = time()
        eval('function' + str(args))
        duration += time() - start
        
    if show:
        print(duration)
    
    return duration
```



[back to toolkit](/toolkit_page)
