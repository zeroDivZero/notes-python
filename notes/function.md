# FUNCTION

## Declaration

```python
def approximate_size(size, a_kilobyte_is_1024_bytes=True):
```

No return type defined. Returns `None` by default. No data type specified for argument. Can provide default value for optional argument.

## Invocation

```python
approximate_size(1000000000000, False)
```

Order of arguments doesn't matter with named arguments, but all arguments to right of first named argument must be named arguments too.

```python
approximate_size(a_kilobyte_is_1024_bytes=False, size=4000)
```

If function needs to update global, be sure to declare it:

```python
x_pos = 0

def move():
  global x_pos
  x_pos += 1
```

## Documentation String

Document function with docstring.

```python
def approximate_size(size, a_kilobyte_is_1024_bytes=True):
    '''Convert a file size to human-readable form.

    Keyword arguments:
    size -- file size in bytes
    a_kilobyte_is_1024_bytes -- if True (default), use multiples of 1024
                                if False, use multiples of 1000

    Returns: string
    '''
```

Optional but recommended. Must start from first line of function. Triple quotes signify multi-line string. Also useful if string contains both single and double quotes. docstring is available at runtime as attribute of function (`__doc__`).

```python
import humansize
print(humansize.approximate_size.__doc__)
```
