# `exists`

```python
os.path.exists(path)
```

Returns `True` if `path` refers to existing path or open file descriptor. Returns `False` for broken symbolic links. On some platforms, may return `False` if permission not granted to execute `os.stat()` on requested file, even if path physically exists.

```python
from os.path import exists

if exists(fname):
  f = open(fname)
```
