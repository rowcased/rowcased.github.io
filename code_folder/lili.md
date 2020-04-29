## List / Linked List Converter

I created this while studying linked lists because
at the time I needed a way to compare the two types.

```python
class Node:
    def __init__(self, current_value, next_value=None):
        self.value = current_value
        self.next  = next_value

def lili(li):
    ''' converts a list into a linked list or
        converts a linked list into a list,
        depending on which type is input '''
    if isinstance(li, list):
        output = None
        while li:
            output = Node(li.pop(), output)
    else:
        output = []
        while li:
            output.append(li.value)
            li = li.next
    return output
```



[back to toolkit](/toolkit)
