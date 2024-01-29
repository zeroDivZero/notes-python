# `argv`

**Argument variable**. List of command line arguments passed to script. If available, script name and arguments are assigned as strings to `argv` in module `sys`.

* `sys.argv[0]` is script name, or empty string if no script and no arguments given.

* If using standard input, `argv[0]` is `-`. If using `-c` command, `argv[0]` is `-c`.

* If using `-m <module>`, `argv[0]` is full module name.

* Options found after `-c` or `-m` are not consumed by interpreter but left in `argv`.

## Example

```python
from sys import argv

script_name, file_name, another_option, last_arg = argv  # unpack
```
