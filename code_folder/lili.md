## List / Linked List Converter

I created this while studying linked lists because
at the time I needed a way to compare the two types.

```python
class Node:
    def __init__(self,val,at_bat=None):
        self.value = val
        self.next  = at_bat

def lili(li):
    ''' converts a list into a linked list or
        converts a linked list into a list,
        depending on which type is input '''
    if type(li) == list:
        output = None
        while li:
            output = Node(li.pop(),output)
    else:
        output = []
        while li:
            output.append(li.value)
            li = li.next
    return output
```



[back to toolkit](/toolkit)
