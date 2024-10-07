# `dict`

```python
record = {'name': 'Randy', 'age': 45, 'height': 5 * 12 + 11}
print(record['name'])  # Randy
print(record['height'])  # 71

record['city'] = 'SF'  # add value
record[1] = 'Apple'  # key doesn't have to be string
record[2] = 'Banana'
del record[1]  # remove value
```

## `KeyError`

Accessing field of missing key.

```python
print(record['state'])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'state'
```

To avoid this error, can use `get()` that returns `None` if key doesn't exist.

```python
print(record.get('state'))  # None
print(record.get('state', 'Does not exist'))  # default value if key missing
```

## Iterate Items

```python
for key, val in list(record.items()):
  print(f'key: {key}, value: {val}')
```
