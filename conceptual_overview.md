# Overview

## Common gotchas

### Iterating through elements

#### Dealing with comments

There's no way to use duck-typing to distinguish between a **NavigableString** and a **Comment**, because they expose the same members (**Comment** inherits from **NavigableString**). If you need to identify one or the other to make your logic work, you need to check its actual type:

```python
if type(some_element) == bs4.element.Comment:
    print('This one's a Comment')
```
