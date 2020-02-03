## Function Timer

Before I knew about the timeit() function, I simply
created something myself, which I used a great deal
while learning how to optimize my code.

<!--    # <-- write declaration to compare multiple of same  -->
```python
def timer(function, args=None, reps=1, show=True):

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
