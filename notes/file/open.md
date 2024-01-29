# `open()`

Opens file and returns file object. Takes many params, but only file path is required.

```python
f = open('workfile', 'w', encoding="utf-8")
```

## `mode`

Param specifying mode file is opened. Defaults to `'r'`, which means open for reading in text mode. Other common values are `'w'` for writing (truncating file if it already exists), `'x'` for exclusive creation, and `'a'` for appending (which on some Unix systems, means that all writes append to end of file regardless of current seek position). In text mode, if encoding not specified, uses platform-dependent current locale encoding. For reading and writing raw bytes use binary mode (`'b'`) and leave encoding unspecified.
