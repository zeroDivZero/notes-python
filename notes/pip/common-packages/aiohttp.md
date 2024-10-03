# `aiohttp`

Built on top of `asyncio`, Python's async programming framework, using **async/await** pattern. Runs multiple non-blocking tasks asynchronously in event loop (on single thread, not multithreaded), by allowing them to suspend and resume execution voluntarily -- cooperative multitasking (not hogging CPU). Different from threads, which require preemptive scheduler to manage context switching between them.

Supports **connection pooling**, feature allowing multiple requests to use same connection, for better performance.

```python
import asyncio
import aiohttp

async def download_file(url):
  async with aiohttp.ClientSession() as session:
    async with session.get(url) as response:
      if 'content-disposition' in response.headers:
        header = response.headers['content-disposition']
        filename = header.split('filename=')[1]
      else:
        filename = url.split('/')[-1]

      with open(filename, mode='wb') as file:
        while True:
          chunk = await response.content.read()
          if not chunk:
            break
          file.write(chunk)

        print(f'Downloaded file {filename}')
```

`await` indicates chunk read operation is async and other tasks can execute in parallel until data is available.

```python
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

async def main():
  tasks = [download_file(url) for url in urls]
  await asyncio.gather(*tasks)

asyncio.run(main())
```

`asyncio.gather()` waits until all tasks in list are completed. `asyncio.run()` initiates and executes async tasks in event loop.
