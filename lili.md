here ya go

```python
class Node:
    def __init__(self,val,at_bat=None):
        self.value = val
        self.next  = at_bat

def lili(li):
    ''' converts a list into a linked list
              or a linked list into a list,
        depending on which type is input '''
    if type(li) == list: # any sequence / collections
        output = None
        while li:
            output = Node(li.pop(),output)
    else: # gotta do a try on .value, .next attributes
        output = []
        while li:
            output.append(li.value)
            li = li.next
    return output
```

[back to toolkit](/toolkit_page)
