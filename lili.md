here ya go

```python
def lili(li):
012345678901234567890123456789012345678901234567890123456
    ''' this function converts a list into a linked list
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
