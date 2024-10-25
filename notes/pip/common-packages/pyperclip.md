# `pyperclip`

For copy & paste clipboard functions.

```python
import pyperclip
```

## Access Clipboard

Current clipboard content:

```python
pyperclip.paste()  # 'https://www.wikipedia.org/'
```

Override content:

```python
pyperclip.copy('Hello, world!')
pyperclip.paste()  # 'Hello, world!'
```
