# `for-in`

```python
words = ['cat', 'horse', 'rhinoceros']
for w in words:
    print(w, len(w))
```

Often paired with `range()` for explicit counter:

```python
for i in range(1, 6):
    print(i)
```

If counter not needed, replace with `_`:

```python
for _ in range(50):
    print('Do a pushup')
```

Can use `break` or `continue` to early exit or skip to next.
