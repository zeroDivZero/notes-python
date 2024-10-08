# `random`

## `randrange`

`random.randrange(stop)`
`random.randrange(start, stop[, step])`

Returns randomly selected element from `range(start, stop, step)` with equal distribution. Note not inclusive of `stop`.

## `randint`

`random.randint(a, b)`

Alias for `randrange(a, b+1)`.

```python
import random

for i in range(5):
  print(random.randint(1, 10))
```

## `choice`

`random.choice(seq)`

Returns random element from sequence. If `seq` empty, raises `IndexError`.

## `sample`

`random.sample(seq, k)`

Returns `k`-length list of unique items randomly chosen from `seq`.

## `shuffle`

`random.shuffle(x)`

Shuffles sequence `x` in place.

To shuffle immutable sequence and return new shuffled list, use `sample(x, k=len(x))` instead.
