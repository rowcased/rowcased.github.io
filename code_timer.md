# Code Timer Project

<a href="https://rowcased.github.io/">(return to portfolio)</a>

```python
    








#     write in a function that calculates a good rate of reps














"""
#f = open('file_to_execfile.py')
#f.close()

if f.closed: print('file is closed')
else       : print('file is open!')

#with open("file_to_execfile.py") as f: pass

if f.closed: print('file is closed')
else       : print('file is open!')

from past.builtins import execfile
execfile('file_to_execfile.py')

if f.closed: print('file is closed')
else       : print('file is open!')

input('ok2')"""


### title #############################################################################


'          The Codewars API          '


### contents ##########################################################################


"""
   
   
   '‾‾‾‾ Table of contents ‾‾‾‾'
   '                           '
   '     0. quick_code_space   '
   '     1. title              '
   '     2. contents           '
   '     3. notes              '
   '     4. issues             '
   '     5. setup              '
   '     6. change_name        '
   '     7. parse              '
   '     8. validate           '
   '     9. convert_2to3       '
   '    10. ffing              '
   '    11. time_codes         '
   '    12. print_error_data   '
   '    13. processs_code      '
   '    14. func_names         '
   '    15. control_center     '
   '                           '
   '---------------------------'
   
   
"""


### notes #############################################################################


"""

    so it's great and all that you test for speed. when will you test for space?

    I just realized (beach trip 2018) that my timer judeges the overall time to
    execute all code within the pared block amirite
    therefore, fix it if in fact it is flawed therefor

    write function to compare yourself to current top 10 players on the CW leaderboard

    or to any single player or given group of players,
    or all players in the 10 th percentile,
    either by rank,
    or by comparison to average time,
    or other things

--> I need to be able to send all the code through python 2.7.6 first

    so even if the author was logged in with a later version,
    they get the py2 result

    THEN we run the remaining unvalidated codes through Python 3.4.3
    
    finally, run em through Python 3.6.0, as these are the 3 codewars versions

    this should run all the codes. amirite

    other than what? libraries. test suite. CONSTANTS. funky extra code.

some errors, once acheived... ? 

for ffing show difference in those that flashed but had the wrong answer... or sumfn

rate: difference in error_type if a code does conovert but still does not validate !

WHAT THE FUCK ABOUT COMPILE !!!

>>> # for var in locals        per code, post-exec
>>> # if var in builtins
>>> # check if var = builtin
>>> # if any not, replace!

and do it right away, BECAUSE: if a piece of code passed immediately,
                               it could unwittingly have corrupted a builtin already
 
ACTUALLY after exec of some code, check builtins against buitins copy!!!!!

scipt the processs_code steps

be TOLD if it needs a name change

'fake'             # AssertionError related to what?
'format_duration'  # many 'not matches answer' & os = {} caused loop N0 M0RE!!!!!
'phone'            # appears to be a line continuation problem --- SOLVE IT !!
'strip_url_params' # timing issue with missing value 'x' - FUCKIN SOLVED! w/ nu_scope!

 os is still fucking things up, of course, it's eating up EVERYTHING, like re, etc...
 display results in a compact block, including where I stand against the crowd
 design control switches to choose to see the timer list or not, etc...
 still got multiple coder names shoeing up in timing list
 WHY althusky alone AND with a group?
 may want to automate collecting names for registry

 ITERITEMS

 solve_runes is fucked up <--- AND I FOUND OUT WHY !!
 use total codes solved in Python as a stat
     Ackermann says 727 of 1476 ~ total 414 passed 392 errors 5 fails fails? 

 a piece of code uses the same name as one of my functions
 it becomes replaced when the user code is executed
 this needs to be blocked, possibly by pre-emptively re-naming any match
 or maybe instead re-defining the function of mine? there're many optinos....

 why in the fuck are the results of initial validation not consistent?
 probably because inputs is still getting mutated somehow

 make sure fake_test has a bit of everything and is organized and clear

 2to3 success:
    print
    filter (has no len)
    reduce
 2to3 failure:
    integer division vs. float
    from types import IntType
    <> vs. !=
    translate
    filter (not subscriptable)

# # #       code_vars = set(re.sub("[^\w]", " ",  code).split()) USEFUL CODE

"""


### issues ############################################################################


"""

   __Issues Experienced__

 X Problem 1
    predefined globals <-- similar to global imports, ya?

 X Problem 2
    lambdas <-- non-issue? it's just code that works! tested on suic in alphabetized

 X Problem 3
    user parameter variations <-- just doesn't matter if they're renamed, cool

>X<Problem 4
    presence of 'Â'                    for HOW MANY reasons?! get to know 'em
    this doesn't really seem like a problem anymore

 X Problem 5
    parameter order <-- solved by * args ** kwargs, yrs?

___Problem 6
    altered function name   <-- just have to deal with case by case for now
                                at the end of the day, this is big, because
                                the final program is expected to act purely
                                on the name of the program entered. Perhaps
                                it can be taught to sniff out the function.

 X Problem 7
        null lines <-- got 'em

___Problem 8
    Py2 vs Py3 issues <--- somewhat __SOLVED__! omg i learned 2to3 on this project
    but I doubt I will be able to solve all examples, and the rate is not good
    when i learned about 2to3 i was amazed to discover how much does not work
    i feel like i may start figuring out as much as possible on my own, i.e.:
    in 2.7.6 string module has both ascii_uppercase and uppercase, which look same
    in 3.5.2 string module has only ascii_uppercase, so I can sniff out THIS switch
    and I will make as many as possible happen...
    ***
        1) yu_shan # string.uppercase    2) AnsonTing # from string import uppercase
    ***
        no urlparse   <--- Python 3 uses urllibparse ! ok then (another 2to3 issue)
    ***
        iteritems      <-- replaced with items... 2to3 shit, man: partially solved. 
        'Counter' object has no attribute 'iteritems' (MirzaI in strip_url_parse)
    ***
        ERROR  henryRRR 	 type object 'int' has no attribute 'replace'
    ***
        2to3 doesn't recognize float div problem... AW CRAP
    ***
        codewars does not inform me of which version of Python the coder used...
        otherwise I suppose I could get them all and compare speeds accordingly
        ...and have fewer failures (if any!)

    yes, I should run the codes through all versions of Python used by Codewars
    perhaps even giving the author the benefit of the doubt by awarding them the
    best time run from all the different versions: 2.7.6, 3.4.3, 3.6.0


___Problem 9
    Py3.x Py3.y  <--- what will happen here... we'll see, may have to FIND 'em...
    would, when the time comes, apparently be solved by the above

 X Problem 10
    basic imports           <-- solved!

 X Problem 11
    conflicting imports?    <-- no problem, right? because it's per code

 X Problem 12
    comma seperated imports <-- NOT YET... soon. SOLVED !! attempt and import!
    
___Problem 13
    unimports like numpy  <-- Uh, 'NO'. what choice have I but to pre-import by case? 
    ...well, possibly a dynamic importer, but that's bad practice

 X Problem 14
    encoding ©           <--  solved!

 X Problem 15
    non-ASCII names ?!   <--  solved! DUH ...wow ylyl

 X Problem 16
    co-def's not global  <--  solved through pre-exec()

___Problem 17
    string literals      <--  uh, not a problem anynore?  CHECK THESE

___Problem 18
    quotation marks       ... until it comes up !           TWO OUT

 X Problem 19
    Loading more solutions...        <--- aahahahahaha solved... probably good enough?
    Click to view invalid solutions  <--- same!

 X Problem 20
    no print! <-- adapted stockoverflow. at last, a huge problem neatly solved
                 and for that matter, greatly improved since then into tester!   
 X Problem 21
    DEFAULT param ?!      <-- cool problem to find - wait, WHAT probelm? heh-heh

>X<Problem 22
    use of codewars test suite... hm. hadn't considered that. i can get it, right?
    WHY YES I CAN, PROBLEM SOLVED

 X Problem 23
    a user mutates the input data <-- hopefully just refresh? YES! FACT! SOLVED!
    looks like the .split() function is the culprit, will have to check that out
   
 X Problem 24
    multi-line printings...      fangs073 in solve_runes:
        print ((term1[0].lstrip('-') != '?' or len(term1) == 1),
        (term2[0].lstrip('-') != '?' or len(term2) == 1),
        (result[0].lstrip('-') != '?' or len(result) == 1))         solved!

 X Problem 25
    multi-line expressions... appears to be solved? test for it   ...  SOLVED
    return reduce(add\
                  ,map(lambda (_,v): [v + word  for word in get_words(make_hash_from_pairs(remove_letters(key_letter_pair, v)))]\
                       , key_letter_pair)) <--THIS WAS FILTER PROBLEM (2to3 fixed it!)

 X Problem 26
    comments containing non-ascii     <---  their code works, but must handle this...
                                                        SOLVED w/correct encoding !!1!
 X Problem 27
    strings containing non-ascii that are NOT manipulated
                                                               SOMEHOW SOLVED!!1!1111
___Problem 28
    string containing non-ascii that ARE manipulated  ...  NOT solved yet, fuuuuck.
    well, maybe 3.6.0 will automatically have it
    
___Probelm 29
    non-ascii code  <-- hasn't officially come up yet, but I DID it once. FIND THAT
    again, looks like a duplicate problem

___Problem 30
     IndentationError <-- i do NOT like code with 2 not 4 spaces, meanwhile
                          codewars is actually displaying misindented code
                          THIS IS A BIG PROBLEM: i can't count on my source
    TrixxxyFybon in two_sum
    i can replace tabs with 4 spaces... what'll that wreck? ...UH, THERE ARE NO TABS...
    also: I appear to get BAD CODE from codewars... what else can I do but reject it.
    this is a problem. i don't want to fix code by hand, i just want it all to work.

___Problem 31
    my API can't handle a Class challenge  <--- grrr not good, gotta figure a way...
    ...im pretty surer it can learn if you teahc it. nut some setups are involved

 X Problem 32
    funct name from user code matches API name <-- oooh, interesting problem
          qubies validate in solve_runes
                                          also applies to ANY name! of mine. oooh!
    some ASS: def tuple(x)     W T FFF  - must prevent redefining ALL_DATA_STRUCTURES!
    probably because of attempt sanitation / sterility this is now SOLVED
    it has already been brought up: validate is created as a func in some code
                                    and it replaces validate in my test environment
    this is the kid of thing that has to be dealt with prior to exec
    otherwise it will require scripting the antidote
    it has already been brought up: validate is created as a func in some code
                                    and it replaces validate in my test environment
    this is the kid of thing that has to be dealt with prior to exec
    otherwise it will require scripting the antidote

 X Problem 33
    inconsistent results in codes... possibly mutated inputs all over again? SOLVED!

___Problem 34
    individually running 2to3 as files is slow ~ figure out how to "the other way"'
    yet another duplicate...problem 8

 X Problem 35
    " 'dict' object is not callable snuck past my defences to crash the program "
    this happend because someone used a BAD PRACTICE of using the variable 'os'
    which is the name of a major Python module. so STUPID, and it proves the point.
    first I thought I could just replace the one I used for this API. os i did (sic).
    but someone could use a module name I don't use and fuck it up for everyone else
    so how do i protect them all? I'd have to use a complete list of some form...

    I could first gather all the names in any import line of code,
    then add those to a registry to prevent other code from renaming...
    I suppose the only problem is if an individual renames their own import!

    it appears that I have fixed this with a SINGLE name replacement...
        locals() vs. globals(), putting the danger into an isolated scope. WOW.

 X Problem 36
    use of ;     I think I have it solved  <--- WELL, TEST IT!!1!   ok    DID

 X Problem 37
     making use of a built-in variable        as in road_kill...  <-- use import *
    
___Problem 38
    just OBTAINING a built-in variable        as in road_kill...
            how do I gather preloaded shit from codewars?  and add it to my _test ?
    ... oh that sounds lik a headache. like, not unsolvable but WOAH man

 X Problem 39
    inputs or answer needs adjustment or attention, in one case: multiple answers ok
    wow, just make answer an *args tuple like inputs already is!!
    or at least adaptive to type(answer)

 X Problem 40
    bad code that enters an infinite loop         solved through timeout_decorator
    (as in 'ASTP001' in escape_the_mines)         (now it times out after 13 secs)

 X Problem 41
    major issue with scoping I GUESS              ffing is driving me CRAZY

    this has been the most frustrating component of this entire project to date.
    stackoverflow:  "The del statement is for wizards only."  –  S.Lott
    trying to manage locals/globals namespaces was maddening, but I learned a lot
    this issue was solved but only by (eventually) giving up on my exec import method
    compile came up, but dunno if I'll need that, haven't even checked it out yet
    i found runpy. its expected that this will revolutionize the project entirely

 X Problem 42
    FutureWarning make an appearance                    not anymore

___Problem 43
    codes get converted for print 2to3 but DON'T ALWAYS PASS after conversion
    DatabaseMonkey & mislom in parse_url_params
    again: problem 8

___Problem 44
    if someone tries to use Pythin 2 dict items as a list of tuples it will fail
    python 3 has a new class type dict_items which has different rules...
    problem 8

___Problem 43
    on long problems, TimeoutError should prevent Validation for that pice of code
    ... or flashing. damn! f that

Tefferson in escape_the_mines:
i=0
results=[[],['right'],['right', 'down']]  # this is code that fails
def escape_the_mines(map, miner, exit):   # why is it allowed to show
  global i
  t=i
  i=t+1
  return results[t]

WHA THE FUQ:
this was the first piece of code in solve_runes:

implant

def solve_runes(runes):
    print runes
    return

:WHA THE FUQ

* * - - - - - * * DUDE CHIDES IN COMMENT FOR NOT HAVING re ON TAP, FUCKS UP MY CODE:
MMMAAANNN

def dashatize(num):
    return ''.join(
                   (char, '-%s-' % char)[char in '13579']    (UNTIL I FIXED MY CODE)
                   for char in str(num)
                  ).strip('-').replace('--', '-')

# Have to import re because test cases need it.
# Please import re in test suite yourself!
import re
Best Practices1Clever1
0ForkCompare with your solutionLink
 * * _ _ _ _ _ _ _ * *

 * * _ _ _ _ _ _ _ * * DUDE DOES WHAT I DO !
kjmosher

import re  # Error in test suite?  "'re' is not defined" even though I don't use re?

# One-liner, just for shiggles:

dashatize = lambda num: 'None' if num is None else __import__('functools').reduce(lambda a, u: a.replace(u, '-{}-'.format(u)), '13579', str(abs(num))).replace('--', '-').strip('-')

# Readable version:

#def dashatize(num): 
#    if num is None:
#        return 'None'
#    s = str(abs(num))
#    for d in '13579':
#        s = s.replace(d, '-{}-'.format(d))
#    s = s.replace('--', '-')
#    s = s.strip('-')
#    return s
Best Practices0Clever0
0ForkCompare with your solutionLink
 * * _ _ _ _ _ _ _ * *

...during my journey I found some weird shit:
    take this piece of code for "strip_ulr_params" by --> user4542229
import sys
test.assert_equals(1 ,1) <-- they uses a codewars test func to just cheat for points
sys.exit(1)              <-- and for some reason exits Python as an implied failure.

...and the same trick from --> Jafaar from afar (!) except simply exit()

test.assert_equals(1, 1, "Hello")
exit()

what is the max length of a codewars name?
(could program by longest known in myBase)
seems to be 20 chars, at least that many

shrab & crimp soup HAHA!

"""


#    ...  if a coder posts a lot, use their fastest


### setup #############################################################################


from tester import qp, ip, dirp, timer, qlp, nop, pon, dot   # shiz_mod tools!

from sys import stdout          # (one name at a time)
import sys                      # to get error info, to mute printing, for program exit
import os                       # to run file commands in the terminal
import subprocess               # to convert py2 to py 3
from copy import deepcopy       # to skirt mutated input



import re
import inspect
#import time
import timeout_decorator        # timeout_decorator_shiz on the way?
import warnings
import itertools

warnings.filterwarnings("ignore", category=FutureWarning)

from runpy import run_path as run   #   <---   FUCK YEAH   !!!


# at one point, reduce was not recognized... how to other than:

#from functools import reduce
import functools
from functools import *

import string

'ascii_letters', 'ascii_lowercase', 'ascii_uppercase'

# need to import from python 2 I guess:
# letters, translate, maketrans, uppercase, lowercase
"""
Unnamed

import string

def drunk_friend(s):
    if not isinstance(s, str):
        return 'Input is not a string'
    return s.translate(string.maketrans(
        string.ascii_lowercase + string.ascii_uppercase,
        string.ascii_lowercase[::-1] + string.ascii_uppercase[::-1]))
"""



# with neither, rot13b produced 1447 / 1663 timed results @ 87%

# OMG chekc this shit out

"""import builtins
from builtins import *

qp(len(dir(builtins)))
ip('sna')

import past.builtins # duh, no different ...

# and then this

from past.builtins import *

# and then both !!!

qp(len(dir(builtins)))
ip('fu')

import builtins
from builtins import *

qp(len(dir(builtins)))
ip('bar')"""


### change name #######################################################################


def rename(old, new):
    
    '''   rename docstring   '''
    
    with open(new + '_raw.py','r', encoding = ('UTF-8')) as file: raw = file.read()
    raw = raw.replace(old, new)
    with open(new + '_raw.py','w', encoding = ('UTF-8')) as file: file.write(raw)

'''#
old_name = 'fib'
new_name = 'fibonacci_reloaded'
rename(old_name, new_name)
#'''#


#### parse ############################################################################


def parse(name):
    
    '''   this function parses string data copied & pasted from the website
          and returns a dictionary of untested codes keyed by their authors   '''


    "Click to view invalid solutions"


    codes = {}
    with open(name + '_raw.py', encoding = 'UTF-8') as file: raws = file.read()
    raws = raws.replace("iteritems", "items")
    raws = raws.replace("xrange", "range")
    while "import uppercase as" in raws:
        raws = raws.replace("import uppercase as", "import ascii_uppercase as")
    raws = raws.replace("import uppercase", "import ascii_uppercase")
    """print(raws)
    ip()
    print("\n\n\n\n")"""
    raws = raws.replace("Click to view invalid solutions", "")
    """print(raws)
    ip()"""
    raws = raws[1:].split("Oldest")[1].split("©")[0]
    if raws[1] == '\n':
        raws = '\n'.join(line[4:] for line in raws.split("\n") if line)
    raws = ("Link\n" + raws).split("Best Practices")
    raws = [raw.split("Link\n")[1] for raw in raws]
    dot(len(raws))
    while raws:
        dot()
        code = raws.pop(0).split('\n')
        #if code == "\n":
#            ip("lweiubgwljehrbvlkejrbvqlejrhbvaejhbvelqkarjbvlearkjbhlaerhbk")            
        for i,line in enumerate(code):
            if "print " in line:
                code[i] = '#' + line
        if code != [''] and code[-2] == "Show Variations":
            code = code[:-3]
        if not code[0]:
            code = code[1:]
            for i,line in enumerate(code):
                code[i] = line[4:]
        if code and code != ['']:
            #print('-'*87)
            #print(code)
            #print('-'*87)
            coder = code.pop(0)
            code = '\n'.join(code)

            if coder == 'nope' and 'nah' in {'rowcased', 'Blind4Basics', 'jsheng1996',
                         'Hawkfeather', 'FArekkusu', 'jamad', 'hmikihth',
                         'CopperWye','siebenschlaefer', 'KenKamau'}: pass
            if coder in ['@aritra_munsi', 'pastelblue']:
                continue
            codes[coder] = code
    return codes


### validate ##########################################################################


def validate(name, codes, errs, lenpar, inputs):

    '''   validate docstring   '''

    def log_error(coder, error, station):

        '''   log_error docstring   '''
        
        if repr(error) == 'TimeoutError()':
            error_type = 'TimeoutError'
            error = 'times out at 13 seconds'
        elif type(error) == str:
            error_type = 'CodeError'
        else:
            error_type = str(type(error))[8:-2]
            error = str(error)
        if error and error[-1] == ')':
            if 'line' in error:
                linum = int(error[error.index('line ') + 5:-1]) - 1
                line = codes[coder].split('\n')[linum]
                coder += ' ' * (22 - len(coder)) + line.lstrip()
            else:
                coder += ' ' * (20 - len(coder)) + '(' + error[error.index('(') + 11:]
            error = error[:error.index('(')]
        if error_type not in errors:
            errors[error_type] = {error: {coder + ' ' + station}}
        elif error not in errors[error_type]:
            errors[error_type][error] = {coder + ' ' + station}
        else:
            errors[error_type][error].add(coder + ' ' + station)


    @timeout_decorator.timeout(13, use_signals=True)
    def attempt(name, coder, code, inputs, past_build=None):
        #print("START ATTEMPT")
        
        '''   attempt docstring   '''

        #print("inputs = {} type = {}".format(inputs, type(inputs)))
        

        outcome = False
        exec("import " + name + "_test")
        if past_build:
            exec('from past.builtins import PY3, __all__, __builtins__, __cached__, __doc__, __file__, __loader__, __name__, __package__, __path__, __spec__, apply, basestring, chr, cmp, dict, execfile, filter, intern, long, map, misc, noniterators, oct, range, raw_input, reduce, reload, str, unichr, unicode, utils, xrange, zip')
            False
        nop()
        try:
            exec(code,locals())
        except AssertionError as asser:
            log_error(coder,asser,'1')
        except:
            log_error(coder,sys.exc_info()[1],'2')
        else:
            try:
                pon()
                #print("before")
                #print("inputs =", inputs, type(inputs))
                nop()

                


                
                func_ans = eval(name)(*deepcopy(inputs,)) # HERE, OMG!
                pon()
                #print("func_ans =", func_ans, type(func_ans))
                #print("after")
                nop()
                #print(func_ans)
                see_answer = 0
                if see_answer: pon() ; qp(func_ans) ; nop()
            except:
                #pon()
                #print("coder -->%s<--" % coder)
                #print()
                #print("code -->%s<--" % code)
                #nop()
 #               ip('sheeeeit')
                log_error(coder,sys.exc_info()[1],'3')
            else:
                #pon()
                #qp(coder)
                #qp(code)
                #nop()
                if func_ans in answer: # <--- cannot manage a matrix ?!
                    """ValueError: The truth value of an array with more than
                             one element is ambiguous. Use a.any() or a.all()"""
                    outcome = True
                    """if coder == 'rowcased':
                        pon()
                        qp(func_ans)
                        qp(answer)
  #                      ip("shitcakes")
                        nop()"""

                else:
                    """print(func_ans)
                    pon()
                    qp(func_ans)
                    nop()
                    ip('hiya')"""
                    log_error(coder,'result does not match expected answer','4')
                    #"""#
                    if coder == 'Fineax':#'donaldsebleung':
                        pon()
                        print("\n")
                        qp(func_ans)
                        qp(answer)
                        print("\n")
                        nop()
                    #"""#
                        
        pon()
        if past_build:
            from builtins import oct, str, dict, __spec__, __package__, __doc__, map, chr, range, __name__, filter, __loader__, zip
        #print("  FINISH ATTEMPT\n\n")
        return outcome

    print(' Validating (%s) ' % len(codes), end='')
    passed = {}
    failed = {}
    errors = {}
    exec('from ' + name + '_test import *', globals())
    dot(len(codes))
    for coder in codes:
        
        dot()
        #print("before")
        passfail_1 = attempt(name, coder, codes[coder], inputs)
        #print("after")
        if passfail_1 == True:
            passed[coder] = codes[coder]
        else:
            failed[coder] = codes[coder]
    if not failed: percent = '100'
    else         : percent = round((len(passed)/len(codes))*100)
    global total_passed
    if passed: total_passed = {**total_passed, **passed}
    globcent = round((len(total_passed)/lenpar)*100)
    print(' %s codes validated.   (%s%%) \tTotal: %s'\
          % (len(passed), percent, globcent))
    if errs and errors: print_error_data(errors)

    return passed, failed, errors


### run_2to3 ##########################################################################


def convert_2to3(failures): # change iteritems to items, figure out / vs //, filter, et

    '''   run_2to3 docstring here   '''

    print(' Converting (%s) ' % len(failures), end='')
    converted = {}
    noconvert = {}
    lenf = len(failures)
    dot(lenf)
    for coder in failures:
        dot()
        code = failures[coder]
        with open('attempt_2to3.py', 'w', encoding = ('UTF-8')) as x: x.write(code)
        try   : subprocess.check_output('2to3 -w attempt_2to3.py', shell=True)
        except: noconvert[coder] = code
        else  :
            with open('attempt_2to3.py','r',encoding=('UTF-8')) as x:code=x.read()
            converted[coder] = code
    if not noconvert: concent = '100'
    else            : concent = round((len(converted) / lenf) * 100)
    print(' %s codes converted.   (%s%%)' % (len(converted), concent))
    return converted, noconvert


### flash-filing ##########################################################################


def ffing(name, codes, errs, lenp, inputs):

    '''   ffing docstring   '''

    def log_error(coder, error, station):

        '''   log_error docstring   '''
        
        if repr(error) == 'TimeoutError()':
            error_type = 'TimeoutError'
            error = 'times out at 13 seconds'
        elif type(error) == str:
            error_type = 'CodeError'
        else:
            error_type = str(type(error))[8:-2]
            error = str(error)
        if error and error[-1] == ')':
            if 'line' in error:
                qp(error)
                linum = int(error[error.index('line ') + 5:-1]) - 1
                qp(linum)
                scrunch = codes[coder].split('\n')
                qp(len(scrunch))
                qp(coder)
                qp(codes[coder])
                try:
                    line = codes[coder].split('\n')[linum]
                except SyntaxError:
                    print('\n    NOT SILENT!\n')
                    #pass
                except IndexError:
                    print('\n    ALSO LOUD!\n')
                    print(linum,'\n')
                else:
                    coder += ' ' * (22 - len(coder)) + line.lstrip()
            else:
                coder += ' ' * (20 - len(coder)) + '(' + error[error.index('(') + 11:]
            error = error[:error.index('(')]
        if error_type not in errors:
            errors[error_type] = {error: {coder + ' ' + station}}
        elif error not in errors[error_type]:
            errors[error_type][error] = {coder + ' ' + station}
        else:
            errors[error_type][error].add(coder + ' ' + station)

    @timeout_decorator.timeout(13, use_signals=True)
    def affempf(dat_name):
       
        '''   attempt docstring   '''
        
        nop()
        try:
            file_globals = run(dat_name + "_temp.py")
        except SyntaxError:
            failed[coder] = code
            log_error(coder,sys.exc_info()[1],'0')
        except IndexError:
            failed[coder] = code
            log_error(coder,sys.exc_info()[1],'1')
        except:
            failed[coder] = code
            log_error(coder,sys.exc_info()[1],'2')
        else:
            if file_globals['truth'] == True:
                passed[coder] = code
            else:
                failed[coder] = code
                log_error(coder,sys.exc_info()[1],'3')
        pon()
    
    print(' Flashing   (%s)' % len(codes), end='')
    passed = {}
    failed = {}
    errors = {}
    with open(name + '_test.py', 'r', encoding = ('UTF-8')) as temp:
        in_out = temp.read()
    capo = in_out + 'func_name = "' + name + '"\n\njack = print\n\ndef print(*_):_\n\n'
    coda = '\n\noutput = ' + name + repr(inputs)\
         + '\n\ntruth = output in answer\n\nprint = jack\n\n' # print(\'the actual truth:\',truth)'
    dot(len(codes))
    for coder in codes:
        dot()
        code = codes[coder]
        script = capo + code + coda
        with open(name+'_temp.py','w',encoding=('UTF-8')) as temp:temp.write(script)
        affempf(name)
    if not failed: ffcent = '100'
    else         : ffcent = round((len(passed)/len(codes))*100)
    global total_passed
    if passed: total_passed = {**total_passed, **passed}
    globcent = round((len(total_passed)/lenp)*100)
    print(' %s codes flashed.     (%s%%) \tTotal: %s' % (len(passed), ffcent, globcent))
    if errs and errors: print_error_data(errors)
    show_resultos = 0
    if show_resultos:
        print('')
        qp(len(passed))
        qp(len(failed))
        print()
        print('supposely "passed" ffing:')
        for coder in sorted(passed):
            print(' ',coder)
        print()
        print('supposely "failed" ffing:')
        for coder in sorted(failed):
            print(' ',coder)
        print()
    return passed, failed, errors


### time_codes ########################################################################


def time_codes(nom, codes, inputs, reps, lenp):
    
    '''   time_codes docstring   '''

    def log_error(coder, error, station):

        '''   log_error docstring   '''
        
        if repr(error) == 'TimeoutError()':
            error_type = 'TimeoutError'
            error = 'times out at 13 seconds'
        elif type(error) == str:
            error_type = 'CodeError'
        else:
            error_type = str(type(error))[8:-2]
            error = str(error)
        if error and error[-1] == ')':
            if 'line' in error:
                linum = int(error[error.index('line ') + 5:-1]) - 1
                line = codes[coder].split('\n')[linum]
                coder += ' ' * (22 - len(coder)) + line.lstrip()
            else:
                coder += ' ' * (20 - len(coder)) + '(' + error[error.index('(') + 11:]
            error = error[:error.index('(')]
        if error_type not in errors:
            errors[error_type] = {error: {coder + ' ' + station}}
        elif error not in errors[error_type]:
            errors[error_type][error] = {coder + ' ' + station}
        else:
            errors[error_type][error].add(coder + ' ' + station)
    
    def execode(nom, coder, reps, inputs, time_out=None):
        
        '''   execode docstring   '''
        
        nop()
        try:
            exec(codes[coder],locals()) # <-- i don't import anything for this to work...
        except:
            print('EXECUTION FAIL')
            exec_fail[coder] = codes[coder]
            print(' '*40,sys.exc_info()[1])
            log_error(coder,sys.exc_info()[1],'1')
        else:
            print('EXECUTION PASS')
            try:
                if coder == "rowcased":
                    #pon()
                    rowcased_ave_place = 420
                    time_out_data = (timer(eval(nom), inputs, reps, show=False) * 100, coder, rowcased_ave_place)
                    """sum_times = 0
                    sum_places = 0
                    for rep in reps:
                        sum_times += timer(eval(nom), inputs, 1, show=False)
                    rowcased_ave_time = sum_times / reps
                    rowcased_ave_place = sum_places / reps
                    time_out_data = [rowcased_ave_time * 100, coder, rowcased_ave_place]
                    qlp(time_out_data)"""
                    #ip('fooooooo')
                    #nop()
                else:
                    some_coder_ave_place = -273
                    time_out_data = (timer(eval(nom), inputs, reps, show=False) * 100, coder, some_coder_ave_place)
                    #pon()
                    #qlp(time_out_data)
                    #ip()
                    #nop()
            except:
                print('TIMING FAIL')
                bad_news = ('\n\t%s\t%s\n' % (coder, sys.exc_info()[1]))
                time_fail[coder] = codes[coder]
                print(sys.exc_info()[1])
                log_error(coder,sys.exc_info()[1],'2')
            else:
                print('TIMING PASS')
                passed[coder] = codes[coder]
                times.append(time_out_data)
        pon()
    passed = {}
    exec_fail = {}
    time_fail = {}
    errors = {}
    print(' Timing     (%s) ' % len(codes), end='')
    times = [] # 0 time_out_data, 1 ???
    dot(len(codes))
    for coder in codes:
        dot()
        execode(nom, coder, reps, inputs)
 #   ip(times)
    failed = {**exec_fail,**time_fail}
    if not failed: tcent = '100'
    else         : tcent = round((len(passed)/len(codes))*100)
    global total_passed
    #if passed: total_passed = {**total_passed, **passed}
    globcent = round(((len(total_passed)-len(failed))/lenp)*100)
    print(' %s codes timed.     (%s%%) \tTotal: %s' % (len(passed), tcent, globcent))
    if errs and errors: print_error_data(errors)
    return sorted(times)


### print error data ##################################################################


def print_error_data(errors):

    '''   print_error_data docstring   '''    
    
    print('\n ERRATA:\n')
    for error_type in sorted(errors):
        print(error_type,'_'*30)
        print()
        for error in sorted(errors[error_type]):
            if error_type != 'AssertionError':
                print(' ',error)
            for coder in sorted(errors[error_type][error]):
                print('    ',coder)
            print()
    print()


### process_code ######################################################################


def processs_code(name, reps=1, status=0, errs=0, count=0):
    
    '''   1) parse codes into dictionary keyed by coder
          2) run all codes through the validator function
          3) send failed codes to 2to3 ~ creates a CONVOS dict
             (replaces the failed dict with the unconverted)
          4) converted codes are resent to validation
             (passed and failed dicts get updated)   '''

    rowcased_ave_place = 42
    rowcased_ave_percentile = 420

    exec('from ' + name + '_test import inputs, answer',globals())
    nop()
    pon()
    print("answer = {} type = {}".format(answer, type(answer)))
    nop()
    pon()
    #nop()
    if count:
        num_ID = " %s)" % count
    else:
        num_ID = ": "
    print('\n   CODE' + num_ID + " " + name + '\n')
    
    results = [] # lenp, used, used_perc, times, rowcased ave place & percentile, 
    global total_passed
    total_passed = {}
    steps = ['Parsing   ',
             'Validating',
             'Converting',
             'Validating',
             'Updating  ',
             'Timing    ']
    
    print(' Parsing    (raw) ', end='')
    parsed = parse(name)
    lenp = len(parsed)
    results.append(lenp)
    print(' %s codes parsed.' % lenp)
    if not parsed:
        ip('no codes! bye.')
        return
    
    passed_1, failed_1, errors_1 = validate(name, parsed, errs, lenp, inputs)
    total_passed = passed_1
    if failed_1:
        converts, uncons = convert_2to3(failed_1)
        if converts:
            passed_2, failed_2, errors_2 = validate(name, converts, errs, lenp, inputs)
            if passed_2:
                total_passed = {**total_passed, **passed_2}
            if failed_2: #: and 2 + 2 == 5:
                passed_3, failed_3, errors_3 = ffing(name, failed_2, errs, lenp, inputs)
                if passed_3:
                    total_passed = {**total_passed, **passed_3}
    
    results.append(time_codes(name, total_passed, inputs, reps, lenp))
    #print("\n    rowcase placed: %s" % rowcased_ave_place)
 #   qlp(results)
    #if status == 0: pon()
    cup = codes_used_percentage = int(len(total_passed) / lenp * 100)
    success_rate = ' %s out of %s codes were used at %s%s' % (len(total_passed),lenp,cup,'%')
    results.append(success_rate)
#    results.append(rowcased_ave_place)
#    results.append(rowcased_ave_percentile)
 #    qlp(results)
    print()
    return results


### names #############################################################################


func_names = '''Ackermann
alphabetic
alphabetized
alternate_sort
anagram_counter
archers_ready
apparently
atheletic_assn_stats
bear_fur
bocce_score
bonus
bonuses
bucket_of
buy_tofu
cake
calc_type
case_id
catalog
centroid
closest_sum
combat
communication_module
consonant_value
convert_bits
convert_hash_to_array
count_deaf_rats
count_inversion
create_anagram
dashatize
decipher_this
decode_morse
digital_cypher
digits
distance_between_points
distinct_digit_year
dollar_to_speech
domain_name
drunk_friend
duck_shoot
equation_reversal
escape_the_mines
even_odd_disparity
factors_range
fake
fibonacci_reloaded
filter_homogenous
find_dup
find_even_index
find_function
find_missing_letter
find_nth_occurrence
find_outlier
find_sum
first_n_smallest
fix_string_case
flatten
framed_reflection
frog_jump
fruit
furthest_distance
get_digits
get_los_angeles_points
get_neighbourhood
get_password
get_words
hexdump
high
how_many_times
increment_string
infect_apple
inside_out
interweave
is_matched
is_pangram
is_sator_square
is_turing_equation
key_strokes
late_clock
locker_run
longest_palindrome
lowest_product
lucky_sevens
majority
major_scale
maximum_product
maze_runner
mem_alloc
men_still_standing
merge
mirror
mxdiflg
multiply_with_restrictions
mutations
my_languages
mystery_function
next_gen
next_happy_year
not_primes
nth_smallest
num_primorial
odd_ones_out
olympic_ring
oracle
order
path_finder_can_you_reach_the_exit
paint_letterboxes
phone
pig_it
player_manager
pop_shift
populate_dict
quicksum
remove_chars
remove_rotten
reverse_and_mirror
reverse_fun
reverse_number
road_kill
rot13a
rot13b
running
score
scrolling_text
sentence
shortest_steps_to_num
simple_decrypt
simple_string_indices
simple_sum_of_pairs
SJF
solve_runes
sorted_comm_by_digs
sort_my_string
sort_the_inner_content
square_digits
square_up
strip_url_params
substring_count
summation
sum_of_a_beach
textin
to_nato
tongues
triple_double
tv_remote
two_sort
two_sum
vowel_indices
who_eats_who'''


# THE RECENTLY CANNED:
# missing
# odd_not_prime
# tiy_fizz_buzz
# odd_not_prime

#qp(len(func_names.split('\n')))

'                     36 ISSUES'

# 'find_ball'          # 'find_missing_letter' # 'mutual_recursion'
# 'frog_jump'          # 'sentence'            # 'fake'
# 'get_words'          # 'path_finder'         # 'rot13 a & b'
# 'reverse_and_mirror' # 'solve_runes'         # 'road_kill' <-- maybe no more?
# 'find_outlier'       # 'remove_chars'        # 'escape_the_mines'
# 'mutual_recursion_F' # 'substring_count'     # 'format_duration' 
# 'cat_on_table'       # 'find_nth_occurrence' # 'running'
# 'populate_dict'      # 'Vector'              # 'recover_secret'
# 'change_case'        # 'min_value'           # 'min_sum'
# 'tick_toward'

"           people are weird combinations of themselves           "


### control center ####################################################################


''' function name is pasted in the string value of (global) subject variable
    if exists (global) output variable is assigned return values from processs_code()
'''
name = ''
#name = "dashatize"#"decipher_this"     ####    <---    keep me 50 from the end, man
#name ="decode_morse"
#name = "find_function"#vowel_indices"
#name = 'digits'
#name = 'longest_palindrome'
#name = 'longestPalindrome'
#name = 'pop_shift'
#name = 'find_dup'
name = 'maximum_product'
name = 'tiy_fizz_buzz'
name = 'score'
name = 'fruit'
name = 'quicksum'
#name = 'simple_string_indices'
name = 'even_odd_disparity'
name = 'atheletic_assn_stats'
name = 'get_live_neighbours_cnt' # conway's game of life
name = 'next_gen'
name = 'path_finder_can_you_reach_the_exit'
name = 'count_deaf_rats'
name = 'distance_between_points'
name = 'num_primorial'
name = 'is_turing_equation'
name = 'to_lover_case'
name = 'jumping_number'
name = 'max_gap'
name = 'next_happy_year'
name = 'major_scale'
name = 'closest_sum'
name = 'nexus'
"""
name = 'get_los_angeles_points'
name = 'capitalize'
name = 'mirror'
name = 'framed_reflection'
name = 'digital_cypher'
name = 'calc_type'
name = 'bucket_of'
"""
name = 'nexus'
name = 'Ackermann'
name = 'alphabetic'
name = None
name = "multiply_with_restrictions"
name = 'simple_sum_of_pairs'
#name = "create_anagram"
#name = 'order'
name = 'digital_cypher'
#name = 'path_finder_can_you_reach_the_exit'
name = 'next_happy_year'
name = 'distinct_digit_year'
name = 'infect_apple'
name = 'delete_digit'
name = 'get_words'
name = 'lucky_sevens'
#name = 'max_sequence'
#name = 'common_array_elements'
#name = 'ranking'
name = 'get_neighbourhood'
name = 'fibonacci_reloaded'
name = 'square_pi'
name = 'is_sator_square'
name = 'shortest_steps_to_num'
name= 'men_still_standing'
name = 'drunk_friend'
name = "mutations"
###name = "bonus"
name = "bonuses"
#name = "reverse_fun"
name = "flatten"
name = "distinct_digit_year"

name = "next_happy_year"
reps = 1000
errs = 0

show_times = 1
status = 0

if name:
    results = processs_code(name, reps, status, errs)
    times_val = ['  Times for %s:\n' % name]
    for i,time in enumerate(results[1]):
        times_val.append(str(i+1)+' \t '+str(time[0])[:4]+' \t '+time[1])
        if time[1] == 'rowcased':
            place = i + 1
    times_val.append('\n')
    times_val = '\n'.join(times_val)
    if show_times: print(times_val)
all_results_0 = {}
all_results_1 = {}
all_results_2 = {}
def results(names, reps=1):
    count = 0
    #rowcased_ave_time = 0
    rowcased_ave_place = 0
    split_names = names.split('\n')
    lensp = len(split_names)
    qp(lensp)
    for name in split_names:
        count += 1
        this_codes_results = processs_code(name, reps, count=count)
        for i,time in enumerate(this_codes_results[1]):
            if time[1] == 'rowcased':
                print("   rowcased placed:", i+1)
                print("\n")
 #               rowcased_ave_time += time[0]
                rowcased_ave_place += i + 1
        """print(type(this_codes_results),len(this_codes_results))
        print(type(this_codes_results[0]),type(this_codes_results[1]),type(this_codes_results[2]))
        qp(this_codes_results[0]);qp(this_codes_results[1]);qp(this_codes_results[2])
        global all_results_0
        all_results_0 = {**all_results_0, **this_codes_results[0]}
        global all_results_1
        all_results_1 = {**all_results_1, **this_codes_results[1]}
        global all_results_2
        all_results_2 = {**all_results_2, **this_codes_results[2]} #results(func_names, reps=1) #qp(len(all_results)) #for coder in sorted(all_results): #    print(coder) #    print('\n')
        """
 #   print("\n\nrowcased average time :", rowcased_ave_time / len(split_names))
    print("rowcased average place:", int(rowcased_ave_place / lensp))
see = 0
if see:
    qlp(all_results_0)
    qlp(all_results_1)
    qlp(all_results_2)
if not name:
    results(func_names, reps)


#######################################################################################


'_____________end of module___________________________________________________________'


```
