# `request`

<https://docs.python.org/3/library/urllib.request.html#module-urllib.request>

Extensible library for opening URLs.

## `urlretrieve()` (legacy)

Copies network object to local file. Returns tuple `(filename, headers)`:

* `filename`: local file name
* `headers` is `HTTPMessage` object representing headers returned by server

```python
from urllib.request import urlretrieve

url = 'https://api.worldbank.org/v2/en/indicator/'\
  'NY.GDP.MKTP.CD?downloadformat=csv'
filename = 'gdp_by_country.zip'

path, headers = urlretrieve(url, filename)

print(f'file path: {path}')
for name, value in headers.items():
  print(f'[{name}]: {value}')
```
