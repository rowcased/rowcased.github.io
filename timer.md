### Timer!

```python
def timer(function, args=None, reps=1, show=True): # <-- write this to compare two or more of the same
    from time import time
    duration = 0    
    for rep in range(reps):
        start = time()
        eval('function' + str(args)) # + '') # <--- ???
        duration += time() - start
    if show:
        print(duration)
    return duration
```



[back to toolkit](/toolkit_page)
