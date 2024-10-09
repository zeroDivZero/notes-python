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

If function needs to update global, declare it:

```python
x_pos = 0

def move():
  global x_pos
  x_pos += 1
```

## Variable Arguments

```python
def foo(*args):
  print(f'{args[0]} {args[1]} {args[2]}')
```

If unpacking, number of params must match exactly:

```python
def foo(*args):
  arg1, arg2 = args
  print(f'{arg1} {arg2}')

foo('Jane', 'Peter')  # must pass exactly 2 params
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

## Call Stack

How Python remembers where to return execution after each function call. When program calls a function, Python creates corresponding frame object on top of call stack. Frame object stores line number of original function call. Call stack isn't stored in any variable; Python handles it implicitly.

When function call returns, Python removes frame object from top of stack and moves execution to line number stored in it. Frame objects are always added to and removed from top.

## Local and Global Scope

Parameters and variables assigned in function exist in that function's local scope. Variables outside functions exist in global scope. Variable is either local or global. Local variables are also stored in frame objects.

Code in local scope can access global variables or local variables of another scope, but local code can access any global. Variables in different scopes can have same name, including local/global.
