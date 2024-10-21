# `pprint`

```python
pprint.pprint(object, stream=None, indent=1, width=80, depth=None, *, compact=False, sort_dicts=True, underscore_numbers=False)
```

Alias for `pp()` with `sort_dicts` set to `True` by default, which sorts dictionaries' keys. Use `pp()` if want it default to `False`.

```python
record = {'name': 'Randy', 'age': 45, 'height': 5 * 12 + 11}
pprint.pprint(record)
```
