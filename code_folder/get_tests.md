## Get Test Data

I wrote this function to input data for tests that were for asserting the validity of an algorithm I was writing while studying on the Code Signal website.
<br>Note: these tests are used in the [code_tester()](/code_folder/code_tester.md) function.
<br>Note: a call to "quick list print" [qlp()](/code_folder/qlp.md) function.

```python
from tester import qlp

def get_tests(num, show=False):
    tests=[]
    tempL=[]
    while len(tests)!=num:
        pars=[]
        print()
        print(' Enter Test',len(tests)+1,'Items:')
        while '' not in pars:
            varin=input(' ')
            if not varin:
                break
            if varin[0]=='[':
                if varin[-1]!=']':
                    tempL.append(eval(varin[1:-2]))
                else:
                    pars.append(eval(varin[:]))
            elif tempL:
                if varin[-1]==']':
                    tempL.append(eval(varin[1:-1]))
                    pars.append(tempL)
                    tempL=[]
                else:
                    tempL.append(eval(varin[1:-2]))
            else:
                pars.append(eval(varin))
        tests.append(pars)
    if show:
        qlp(tests)
    return tests
```



[back to toolkit](/toolkit)
