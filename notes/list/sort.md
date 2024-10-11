# SORT

## `sort`

```python
sort(*, key=None, reverse=False)
```

Sorts in place. `key` specifies function to extract comparison key from each item.

```python
nums = [3.14, -1, 50.0, 999, 2]
nums.sort()  # [-1, 2, 3.14, 50.0, 999]
nums.sort(reverse=True)  # [999, 50.0, 3.14, 2, -1]

words = ['Bill', 'banana', 'apple', 'Ana', 'cantaloupe', 'Cynthia']
words.sort()  # ['Ana', 'Bill', 'Cynthia', 'apple', 'banana', 'cantaloupe']
words.sort(key=str.lower)  # ['Ana', 'apple', 'banana', 'Bill', 'cantaloupe', 'Cynthia']
```

All items must be of comparable types (e.g., no mixing numbers with strings), otherwise `TypeError`.
