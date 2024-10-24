# `join`, `split`

## `join`

Joins list of strings into single string:

```python
', '.join(['apple', 'banana', 'cantaloupe'])  # 'apple, banana, cantaloupe'
```

## `split`

Separates string into list of words, delimited by space (default).

```python
'My name is Randy'.split()  # ['My', 'name', 'is', 'Randy']
```

Change delimiter:

```python
'https://en.wikipedia.org/wiki/Pyramid'.split('/')  # ['https:', '', 'en.wikipedia.org', 'wiki', 'Pyramid']
```
