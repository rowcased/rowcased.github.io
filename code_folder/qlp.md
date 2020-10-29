## Quick Sequence Print

I originally created this as "qlp" (quick list print) to have control over pretty printing lists. At the time I didn't know there was something already available for that. Later I adapted it to handle all sequence types.
<br>Note: it contains a call to the [namer()](/namer.md) function.
<br>Note: qlp is used in the [get_tests()](/get_tests.md) function, among others.

```python
def qsp(thing,sub='',I=1,ind=5,comment=''):
    """ method for displaying items of any sequence  """
    import inspect
    print()
    lent = len(thing)
    head = __import__('toolbox').namer(thing)
    typo = type(thing)
    if typo in [list,tuple,set,dict,frozenset] and len(thing) > 1:
        if typo == list:
            book, ends = '[]'
        elif typo == tuple:
            book, ends = '()'
        else:
            book, ends = '{}'
        print('\n '*I+head+'\t',comment,'\n  ', book, end=' ')
        if sub:
            sub = sub + ' = '
        if type(thing) == dict:
            listo = sorted(thing)
        else:
            listo = thing
        for i, t in enumerate(listo):
            if type(thing) == dict:
                print('\n'*(i not in (0,lent))+' '*ind*(i!=0)+sub+str(t),':',thing[t], end=' ')
            else:
                print('\n'*(i not in (0,lent))+' '*ind*(i!=0)+sub+str(t), end=' ')
        print(ends)
    else:
        print(' '+head,'=',thing)
    print()
```



[back to toolkit](/toolkit)
