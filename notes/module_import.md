# MODULE IMPORT

## Module

Python definitions and statements (usually related) saved in `.py` file. Can be imported to reuse that module's functionality without duplicating code. Module name same as file name. Can be imported to another module or to *main* module (top-level collection of functionality).

## Import

Import entire module:

```python
import mymodule
mymodule.my_function()
```

Can import multiple, separated by commas.

Import specific function:

```python
from mymodule import my_function
my_function()
```

Import all features of module:

```python
from mymodule import *
my_function()
another_function()
```

Generally prefer importing just module name, so usage is clear.

## Standard Library

Set of modules that comes with Python distribution, such as `sys`, `os`, `random`, `re`.

## Third-Party Modules

Such as `request`. Installed with `pip`.

## Import Search Path

Python looks in `sys.path` for module. Can add own search path, typically at top of script, effective through program's life cycle:

```python
import sys

print(sys.path)  # list of directories; Python searches for matching module in order
sys.path.insert(0, '/home/mypython/libs')
```

Watch out for overriding standard library names.
