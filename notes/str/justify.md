# JUSTIFY

Useful for visualization of tabular data.

## `rjust`, `ljust`

Returns padded string to justify content. First argument is integer length:

```python
'Hello'.rjust(10)  # '     Hello'
'Hello, world'.ljust(20)  # 'Hello, world        '
```

Optional second argument for fill character:

```python
'Hello'.ljust(10, '-')  # 'Hello-----'
```

## `center`

```python
>>> 'Hello'.center(20)
'       Hello        '
>>> 'Hello'.center(20, '=')
'=======Hello========'
```
