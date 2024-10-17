# `dedent`

```python
textwrap.dedent(text)
```

Removes common leading whitespace from every line in text.

Makes triple-quoted strings line up on left edge of display, while indented in source code.

Tabs and spaces are treated as whitespace, but not equal: `"  hello"` and `"\thello"` have no common leading whitespace.

Lines containing only whitespace are normalized to single newline character in output.
