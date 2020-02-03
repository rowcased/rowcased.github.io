dor was made for a timing program 


```python
def dot(lens=None):
    if lens:
        if lens < 10:
            print('..........', end='')
            return
        global total
        total = lens
        global count
        count = 0
        global decca
        decca = 10
        return lens
    try:
        count
    except NameError:
        #print('   ***  (nope)  ***')
        return
    if decca == 100:
        return
    count += 1
    percent = round(count/total*100)
    if percent >= decca:
        print('.',end='')
        decca += 10
    return count
```


[back to toolkit](/toolkit_page)
