## Progress Dots

This program was made for a timing program,
and thus part of a larger program, "codewars code timer".


```python
def dot(lens=None):

   ''' prints dots based on progress of a process '''

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
<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

[back to toolkit](/toolkit_page)
