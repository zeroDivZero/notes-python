# PREFIX, SUFFIX

## `startswith`, `endswith`

Returns `True` if string starts or ends (respectively) with passed-in value.

```python
'Hello, world!'.startswith('Hello,')  # True
'Hello, world!'.endswith('world')  # False
```

## `removeprefix`, `removesuffix`

```python
'https://nostarch.com'.removeprefix('https://')  # nostarch.com
'nostarch.com'.removesuffix('.com')  # nostarch
```
