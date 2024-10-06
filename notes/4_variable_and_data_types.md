# VARIABLE AND DATA TYPES

Dynamic type. Type implicitly set when assigned.

## Common Types

Boolean: `bool`
Number: `int`, `float` (no double)
String: `str`
Sequence: `list`, `tuple`
Mapping: `dict`
Set: `set`
Binary: `bytes`
`None`: `NoneType`

## Boolean

```python
is_game_over = False
```

Value either `True` or `False`. Case-sensitive.

## Number

```python
num_lives = 3
percent_health = 0.75
```

## String

```python
player_name = "Peter"  # single quotes also acceptable
```

## `None`

Represents *nothing*, or *value-without-value*. Only value of `NoneType`. `null`, `nil`, `undefined` in other languages. Return value of functions that don't return anything.

## Determining Type

```python
print(type(player_name))  # <class 'str'>
```
