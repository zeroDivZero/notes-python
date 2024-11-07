# `re`

Provides regular expression matching operations.

```python
import re
```

## `Regex` Object

Pass regex to `re.compile()` to get object:

```python
phone_regex = re.compile(r'\d{3}-\d{3}-\d{4}')
```

## Match

Pass string to `Regex` object's `search()`.

`Match` object if match found. Use its `group()` method to get matched text. `None` if no match.

```python
mo = phone_regex.search('My number is 858-555-4242.')
print('Phone number found: ' + mo.group())  # Phone number found: 858-555-4242
```
