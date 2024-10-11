# `enumerate`

```python
enumerate(iterable, start=0)
```

Returns enumerate object that can be converted to list of tuples of (index, value) pair.

```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']
list(enumerate(seasons))  # [(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
list(enumerate(seasons, start=1))  # [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]
```

```python
players = ['John', 'Adam', 'Natalie', 'Peter']
for index, player in enumerate(players):
  print('Player of index ' + str(index) + ' is: ' + player)
```
