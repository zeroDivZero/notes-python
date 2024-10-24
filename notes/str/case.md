# CASE

## `title()`

```python
print('ada lovelace'.title())  # Ada Lovelace
```

## `lower()`, `upper()`

```python
name = 'Ada Lovelace'
print(name.lower())  # ada lovelace
print(name.upper())  # ADA LOVELACE
```

## `capitalize()`

```python
print('hello, how are you?'.capitalize())  # Hello, how are you?
```

## `islower`, `isupper`

If string has at least 1 letter, and all letters are lower or upper case.

```python
'Hello'.islower()  # False
'HELLO'.isupper()  # True
```

## `istitle`

Returns `True` if string consists only of words beginning with uppercase followed by lowercases.

```python
'Ada Lovelace'.istitle()  # True
```
