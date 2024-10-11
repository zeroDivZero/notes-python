# REMOVE

## Remove by Index - `del`

If index of item to delete is known and don't need it afterward.

```python
motorcycles = ['honda', 'yamaha', 'suzuki']
del motorcycles[1]  # ['honda', 'suzuki']
```

## Remove by Index - `pop`

```python
list.pop([i])
```

Removes item at specified index and returns it. If no index given, `a.pop()` removes and returns last item. `IndexError` if empty list or index out of range.

Removes all items. Equivalent to `del a[:]`.

## Remove by Value - `remove()`

```python
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
motorcycles.remove('suzuki')
print(motorcycles)  # ['honda', 'yamaha', 'ducati']
```

Removes only first occurrence. `ValueError` if value not found.

## Remove All - `clear`

```python
list.clear()
```
