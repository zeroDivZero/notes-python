# `requests`

<https://pypi.org/project/requests/>

HTTP library to send HTTP/1.1 requests. One of the most downloaded Python packages today.

Unlike built-in `urllib`, can make more advanced HTTP requests, such as those requiring authentication. User-friendly and Pythonic, handles low-level network communication underneath.

Flexible and offers more controls. E.g., can specify headers, handle cookies, access data behind login-gated webpages, stream data in chunks, etc.

Efficient and performant. Automatically handles connection pooling and reuse, optimizing network utilization.

## Response Content as Text

If response can be encoded as text.

```python
import requests

response = requests.get('https://api.github.com/events')
t = response.text
```

## Download as File

```python
import requests

url = 'https://api.worldbank.org/v2/en/indicator/NY.GDP.MKTP.CD'
query_params = {'downloadformat': 'csv'}

response = requests.get(url, params=query_params)

with open('gdp_by_country.zip', mode='wb') as file:
  file.write(response.content)
```

## Download Large File as Stream

```python
url = 'https://databank.worldbank.org/data/download/WDI_CSV.zip'
response = requests.get(url, stream=True)
```

Specifying `stream=True` downloads only HTTP response headers first. Print `response.headers` to notice value `{'Connection': 'keep-alive'}`, indicating HTTP persistent connection, which allows multiple requests within single network connection. Re-establishing new TCP/IP connection is expensive.

```python
with open('WDI_CSV.zip', mode='wb') as file:
  for chunk in response.iter_content(chunk_size=10 * 1024):  # 10 kb
    file.write(chunk)
```

Even if not consuming all chunks, use `with` to ensure response remains available and connection gracefully closed when done.

## Parallel Downloads

### `requests` with Thread Pool

```python
from concurrent.futures import ThreadPoolExecutor
import requests

def download_file(url):
  response = requests.get(url)
  if 'content-disposition' in response.headers:
    content_disposition = response.headers['content-disposition']
    filename = content_disposition.split('filename=')[1]
  else:
    filename = url.split('/')[-1]

  with open(filename, mode='wb') as file:
    file.write(response.content)

  print(f'Downloaded file {filename}')

template_url = (
  'https://api.worldbank.org/v2/en/indicator/'
  '{resource}?downloadformat=csv'
)

urls = [
  # total population by country
  template_url.format(resource='SP.POP.TOTL'),

  # GDP by country
  template_url.format(resource='NY.GDP.MKTP.CD'),

  # population density by country
  template_url.format(resource='EN.POP.DNST'),
]

with ThreadPoolExecutor() as executor:
  executor.map(download_file, urls)
```

Executor allocates pool of threads up front and assigns separate thread to each download task.
