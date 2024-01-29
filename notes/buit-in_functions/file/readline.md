# `readline()`

Reads single line from file. Returns empty string if reached end of file, or string with single `\n` (newline) if blank line.

```python
f.readline()
```

## Loop Over Object with `for`

For reading lines, loop over file object. Memory efficient, fast, and leads to simple code:

```python
for line in f:
    print(line, end='')
```

## Read All Lines as List

`list(f)` or `f.readlines()`.
