# `partition`

Splits string into text before and after separator. Returns tuple of **(*before*, *separator*, *after*)**:

```python
'Hello, world!'.partition('world')  # ('Hello, ', 'world', '!')
```

If separator occurs multiple times, string split on first occurrence.

If separator not found, first item in tuple is entire string, with other two empty.
