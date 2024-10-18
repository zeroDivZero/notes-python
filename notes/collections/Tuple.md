# TUPLE

Similar to list but immutable. More often to hold elements of different types.

```python
casepack = ('Soda', 6)
item_name = casepack[0]
```

```python
backpack = ('herb', 'herb', 'potion', 'shovel')
print(backpack.count('herb'))  # 2
print(backpack.index('potion'))  # 2
print(len(backpack))  # 4
```

`TypeError` if attempt to change item value.

Tuples are defined by presence of comma; parentheses only make them more readable. To define tuple with single item:

```python
my_t = (3,)
```
