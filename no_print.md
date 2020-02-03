no_print() and print_on are a program pair.

```python
def no_print():

    ''' this function disables the Python built-in print
        function, print_on is its counterprogram'''
    
    global mess
    mess = sys.stdout
    sys.stdout = open(os.devnull, 'w')



def print_on():

    ''' this function reenables the Python built-in print
        function, no_print is its counterprogram'''

    global mess
    sys.stdout = mess

pon = print_on
nop = no_print

```


[back to toolkit](/toolkit_page)
