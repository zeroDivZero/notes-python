# `str`

String type. Sequence type like `list`, can perform similar operations like indexing and slicing.

```python
name = 'Randy'
x, y, z = name[0], name[-2], name[:3]  # 'R', 'd', 'Ran'
'Ra' in name  # True
'r' in name  # False
'y' not in name  # False

for i in name:
  print('--- ' + i + ' ---')
```

One key difference from `list` is string is immutable. `name[1] = 'e'` returns `TypeError`.
