# `fill`

```python
textwrap.fill(text, width=70, *, initial_indent='', subsequent_indent='', ...
```

Wraps single paragraph in `text`, and returns single string containing wrapped paragraph. Shorthand for

```python
'\n'.join(wrap(text, ...))
```

Accepts same keyword arguments as `wrap()`.
