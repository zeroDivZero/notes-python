# RANGE

List of ascending/descending whole numbers, but doesn't have functionality of list. Usually need to specify start and end values, and optional step value.

```python
zero_to_nine = range(10)
one_to_ten = range(1, 11)
ten_to_one = range(10, 0, -1)
```

## Check if Number in Range

```python
if 0 <= num < 100:
    print('in range')

if num in range(100):
    print('in range')
```
