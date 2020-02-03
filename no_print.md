
no_print()

```python
def no_print():
    '''   The no_print docstring   '''
    global mess
    mess = sys.stdout
    sys.stdout = open(os.devnull, 'w')
nop = no_print

def prant(chat=None):
    def nope(*args):
        pass
    if not chat:
        print = nope

def print_on():
    '''   The print_on docstring   '''
    global mess
    sys.stdout = mess
pon = print_on

```


[back to toolkit](/toolkit_page)
