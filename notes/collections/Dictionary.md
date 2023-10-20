# DICTIONARY

Stores key-value pairs at each index. Each element is tuple of key-value pair. Access values based on keys, not indexes. Has utilities to retrieve list of keys or values. Mutable.

```python
inventory = {'Knife': 1, 'Health Kit': 4, 'Torch': 3}
num_torches = inventory['Torch']
inventory['Torch'] += 1
inventory['Gold'] = 50
```

## `get()`

If not sure key exists:

```python
inventory.get('Rope') # None
```

## All Keys and Values

```python
inventory.keys()
inventory.values()
```

## `pop()`, `clear()`

```python
knives = inventory.pop('Knife') # 1
inventory.clear() # {}
```
