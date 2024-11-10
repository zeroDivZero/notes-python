# `pandas`

Data analysis library.

Import convention:

```python
import pandas as pd
```

## `DataFrame`

Fundamental data structure:

```python
```

2D structure storing data in columns (like spreadsheet). When input is Python dictionary of lists, keys used as column headers and each list as one column.

Printing `DataFrame` displays data in tabular format:

```python
print(df)
```

## `Series`

To access single column (`Series`):

```python
print(df['Name'])
```

To create `Series`:

```python
ages = pd.Series([18, 35, 63], name='Age')
```

## Functions

Example function on `DataFrame` or `Series`:

```python
print(df['Age'].max())
print(ages.max())
```

## Rows

To access top specified number of rows:

```python
df.head(8)
```

Similarly, use `tail()` to get bottom rows.

## Column Data Types

```python
df.dtypes
```

## Numerical Data Statistics

```python
print(df.describe())  # returns a DataFrame
print(ages.describe())  # returns a Series
```

## Technical Info Summary

```python
df.info()
```
