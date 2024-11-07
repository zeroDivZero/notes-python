# `group`

```python
regex = re.compile(r'(\d{3})-(\d{3}-\d{4})')
mo = regex.search('My number is 858-555-4242.')
print(mo.group(1))  # 858
print(mo.group(2))  # 555-4242
```

`mo.group(0)` returns full matched text like `mo.group()`.

`groups()` returns all groups as tuple:

```python
print(mo.groups())  # ('858', '555-4242')
```
