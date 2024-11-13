# `isfile`

```python
os.path.isfile(path)
```

Returns `True` if `path` is an existing regular file. Follows symbolic links, so both `islink()` and `isfile()` can be true for same path.
