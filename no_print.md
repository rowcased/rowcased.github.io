## Print Disabler

This program pairing was created to temporarily 
disable the print function while running a huge
set of codes, some of which _may_ print something.

```python
def no_print():

    ''' this function disables the Python built-in
        print function, counterprogram of print_on '''
    
    global temp_print
    temp_print = sys.stdout
    sys.stdout = open(os.devnull, 'w')

def print_on():

    ''' this function reenables the Python built-in
        print function, counterprogram of no_print '''

    global temp_print
    sys.stdout = temp_print

nop = no_print
pon = print_on

```


[back to toolkit](/toolkit_page)
