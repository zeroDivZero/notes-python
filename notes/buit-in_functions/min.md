# `min`

```python
min(iterable, *, key=None)
min(iterable, *, default, key=None)
min(arg1, arg2, *args, key=None)
```

Returns smallest item in `iterable` or of two or more arguments.

Optional `key` argument specifies one-argument ordering function like that for `list.sort()`. `default` is return object if `iterable`'s empty (otherwise `ValueError`).

If multiple items minimal, returns first one (stable).
