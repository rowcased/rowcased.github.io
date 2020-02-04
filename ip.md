## Input Pause

This little piece of code was a debugging tool.
It just stops the program where you want it to.
You have the option of printing out a message.

```python
def input_pause(text=' ** program paused **'):

    ''' pauses a program by waiting for input
        an optional message can be included'''
        
    input('\n%s\n' % text)

ip = input_pause
```

[back to toolkit](/toolkit_page)
