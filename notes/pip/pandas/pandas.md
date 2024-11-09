# `pandas`

Data analysis library.

Import convention:

```python
import pandas as pd
```

Fundamental data structure `DataFrame`:

```python
```

2D structure storing data in columns (like spreadsheet). When input is Python dictionary of lists, keys used as column headers and each list as one column.

Printing `DataFrame` displays data in tabular format:

```python
print(df)
```

To access single column (`Series`):

```python
print(df['Name'])
```

To create `Series`:

```python
ages = pd.Series([18, 35, 63], name='Age')
```

Example function on `DataFrame` or `Series`:

```python
print(df['Age'].max())
print(ages.max())
```

Basic statistics of numerical data:

```python
print(df.describe())  # returns a DataFrame
print(ages.describe())  # returns a Series
```
