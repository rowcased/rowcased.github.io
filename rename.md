

```python
def rename(old, new):
    
    '''   rename docstring   '''
    
    with open(new + '_raw.py','r', encoding = ('UTF-8')) as file: raw = file.read()
    raw = raw.replace(old, new)
    with open(new + '_raw.py','w', encoding = ('UTF-8')) as file: file.write(raw)
```

