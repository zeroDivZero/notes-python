# FORMATTED STRING

## Formatted String Literal

Begin string with `f` or `F` before opening quotation mark. Inside this string, can write expression between `{` and `}` referencing variables or literal values.

```python
year = 2023
month = 11
day = 25
date_str = f'{day}th Day of {month}th Month of the Year {year}'
```

## `str.format()`

Still uses `{` and `}` to mark substituted variable, can provide detailed formatting directives.

```python
yes_votes = 42_572_654
no_votes = 43_132_495
percentage = yes_votes / (yes_votes + no_votes)
prcnt_str = '{:-9} YES votes  {:2.2%}'.format(yes_votes, percentage)
```
