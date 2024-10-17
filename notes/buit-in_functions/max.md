# `max`

```python
max(iterable, *, key=None)
max(iterable, *, default, key=None)
max(arg1, arg2, *args, key=None)
```

Returns largest item in `iterable` orof two or more arguments.

Optional `key` argument specifies one-argument ordering function like that for `list.sort()`. `default` is return object if `iterable`'s empty (otherwise `ValueError`).

If multiple items maximal, returns first one (stable).
