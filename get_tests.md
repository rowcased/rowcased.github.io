## Get Test Data

I wrote this function to input data for tests that were for asserting the validity of an algorithm I was writing while studying on the Code Signal website.
<br>Note: these tests are used in the testing function: [code_signal_tester()](/code_signal_tester.md) function.

```python
def getests(num):
    tests=[]
    tempL=[]
    while len(tests)!=num:
        pars=[]
        print('\n'+' Enter Test',str(len(tests)+1),'Items:')
        while '' not in pars:
            varin=input(' ')
            if not varin:break
            if varin[0]=='[':
                if varin[-1]!=']':tempL.append(eval(varin[1:-2]))
                else:pars.append(eval(varin[:]))                  
            elif tempL:
                if varin[-1]==']':
                    tempL.append(eval(varin[1:-1]))
                    pars.append(tempL)
                    tempL=[]
                else:tempL.append(eval(varin[1:-2]))
            else:pars.append(eval(varin)) # trips modded here ?1!             
        tests.append(pars)
        pars=[] # OR HERE ?
    for t in tests:
        if t==tests[0]:print('tests = ['+str(t)+',\n')
        elif t==tests[-1]:print('         '+str(t)+']\n')
        else:print('         '+str(t)+',\n')
```



[back to toolkit](/toolkit_page)
