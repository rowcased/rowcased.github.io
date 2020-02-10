## Code Tester

I wrote this program very early on in my study when I was working on a site now called Code Signal.
<br>Note: it uses tests created by user input with this function: [get_tests()](/get_tests.md) function.

```python
def test(code, start=None, stop=None):
    from pprint import pprint, pformat
    from __main__ import tests
    import inspect
    results='.'
    miltime=''
    TEST=''
    ttime=0
    P=[]
    F=[]
    p = True
    GGG = 'Nope'
    HHH = 'Nope'
    if stop == 'nopr':
        GGG = ', '+str(-start)
        start = 1
        p = None
        stop = len(tests)
    elif type(start) != int:
        if stop:
            GGG = ', '+str(stop)
        stop = len(tests)
        if start == 'nopr':
            start = 1
            p = None
        elif not start:
            start = 1
            stop = len(tests)
    elif start > len(tests) or start < 1 or stop != None and start > stop:
        start = 2
        stop = 1
        F = ['Invalid Index Input']
    elif stop == None:
        stop = start
    if p:print('\n'*2+'_'*4+' Codefight: "'+str(code)[10:-16]+'" Results '+'_'*(60-(   len(str(code)[10:-16])     ))+'\n')
    for t in range(start-1,stop):
        milt=0       
        if TEST and p:print('TEST #',(t+1),'\n')
        if GGG != 'Nope':
            result = eval('code('+', '.join(['tests[t]['+str(i)+']' for i in range(len(list(inspect.getargspec(code))[0])-1)])+GGG+')')
        else:
            if code.__defaults__:
                temp = list(code.__defaults__)
                for d,default in enumerate(temp):
                    if type(default) == str:
                        if default != '':
                            temp[d] = repr(default)
                            temp = tuple(temp)
                        else:
                            temp[d] = '\'\''
                    else:
                        None
                result = eval('code('+', '.join(['tests[t]['+str(i)+']'
                                                 for i in range(len(list(inspect.getargspec(code))[0])-len(temp))])+', '+', '.join([str(default)
                                                                                                                                                 for default in temp])+')')
            else:
                result = eval('code('+', '.join(['tests[t]['+str(i)+']'
                                                 for i in range(len(list(inspect.getargspec(code))[0]))])+')')
        answer=tests[t][-1]
        if result==answer:
            verdict='PASS'
            P.append(t+1)
        else:
            verdict='FAIL'
            F.append(t+1)
        if len(str(t+1))<2:
            num=' '+str(t+1)
        else:
            num=str(t+1)
        if miltime:
            True        
        else:
            if p:print('\n'+'  TEST',num,'=',verdict)
        if results:
            if p:print('\n'+'    -->'+str(answer)+'<--'+'\n') # CALCULATED
            if p:print('    -->'+str(result)+'<--'+'\n')
    if p:print('\n'+'    RESULTS')
    PASS_FAIL = False
    if P==[]:
        if p:print('\n'+'      Passed: None')
        pformat(F)
        if p:print('\n'+'      Failed: ',F)
        if p:print('\n'+'      Result: '+str(len(P))+'/'+str((len(P)+len(F)))+' = 0% Correct')
    elif F==[]:
        pformat(P)
        if p:print('\n'+'      Passed: ',P)
        if p:print('\n'+'      Failed: None')
        if p:print('\n'+'      Result: '+str(len(P))+'/'+str((len(P)+len(F)))+' = 100% Correct')
        PASS_FAIL = True
    else:
        pformat(P)
        if p:print('\n'+'      Passed: ',P)
        pformat(F)
        if p:print('\n'+'      Failed: ',F)
        if p:print('\n'+'      Result: '+str(len(P))+'/'+str((len(P)+len(F)))+' = '+str(((len(P)/(len(P)+len(F)))*100))[:2]+'% Correct')
    if miltime:
        ddd=float(milt)/len(progs)
        if p:
            if ddd<4:
                ttest=' PASS'
            else:
                ttest=' FAIL'
        if p:print('\n'+'      Avemil: '+str(ddd)[:4]+ttest+'\n'*2)
    elif p:
        print('\n')
    if p:print('_'*4+' fin '+'_'*78+'\n'*2)
    return PASS_FAIL
```



[back to toolkit](/toolkit_page)
