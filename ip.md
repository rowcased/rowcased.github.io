## Input Pause

While learning to code, I occasionally needed the program
to stop somewhere to make it easier to debug.

```python
def input_pause(text=' ** program paused **'):

    ''' pauses a program by waiting for input
        an optional message can be included'''
        
    input('\n%s\n' % text)

ip = input_pause
```

[back to toolkit](/toolkit_page)
