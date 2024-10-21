# `dict`

Collection data type storing key-value pairs, unordered.

```python
record = {'name': 'Randy', 'age': 45, 'height': 5 * 12 + 11}
print(record['name'])  # Randy
print(record['height'])  # 71

record['city'] = 'SF'  # add value
record[1] = 'Apple'  # key doesn't have to be string
record[2] = 'Banana'
del record[1]  # remove value
```

## Missing Key

`KeyError` if missing key:

```python
print(record['state'])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'state'
```

Can check first if key in dictionary:

```python
key = input('key: ')
if key in record:
    print(record[key])
```

Or use `get()`, which returns `None` if key doesn't exist:

```python
print(record.get('state'))  # None
print(record.get('state', 'Does not exist'))  # default value if key missing
```

## Iterate Keys, Values, Items

`keys()`, `values()`, `items()` each returns object that can be iterated over by, for example, for-loop. Or converted to list with `list()`.

```python
for k in record.keys():
    print(k)

for v in record.values():
    print(v)

for k, v in record.items():  # tuples
    print(f'key: {k}, value: {v}')

print('SF' in record.values())  # True
print(('name', 'Randy') not in record.items())  # False
```

## Default Value

Use `setdefault()` to add value only if key doesn't exist (returns value if key already exists):

```python
record = {'name': 'Randy', 'age': 45}
print(record.setdefault('color', 'black'))  # black
print(record.setdefault('color', 'white'))  # black
```

Easy way to count characters in string:

```python
message = 'It was a bright cold day in April, and the clocks were striking thirteen.'
count = {}

for character in message:
    count.setdefault(character, 0)
    count[character] += 1
```
