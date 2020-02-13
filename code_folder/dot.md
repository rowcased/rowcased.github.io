## Progress Dots

This program was made for a timing program,
and thus part of a larger program, "codewars code timer".


```python
def dot(lens=None):

   ''' prints dots based on the progress of a process.
       first called before a loop with length passed,
       then called with no argument for each iteration.
       each 10th of progress; a progress dot appears'''

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
        print('   ***  (there was no count)  ***')
        return
    if decca == 100:
        return
    count += 1
    percent = round(count / total * 100)
    if percent >= decca:
        print('.', end = '')
        decca += 10
    return count
```


[back to toolkit](/toolkit)
