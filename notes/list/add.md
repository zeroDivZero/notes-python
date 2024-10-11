# ADD

## Concatenation

```python
a_list = ['a']
a_list += 'b'  # ['a', 'b']
a_list += ['c', 'd']  # ['a', 'b', 'c', 'd']
a_list += [['e', 'f'], 'g']  # ['a', 'b', 'c', 'd', ['e', 'f'], 'g']
```

## Replication

```python
a_list = ['X', 'Y', 'Z'] * 3  # ['X', 'Y', 'Z', 'X', 'Y', 'Z', 'X', 'Y', 'Z']
```

## `append`

```python
list.append(x)
```

Adds single item to end.

```python
a_list = ['a', 'b']
a_list.append('c')  # ['a', 'b', 'c']
```

## `extend`

```python
list.extend(iterable)
```

Extends list by appending all items from `iterable`. Equivalent to `a[len(a):] = iterable`.

```python
a_list.extend(['dee', 'Ω'])  # ['a', 'b', 'c', 'dee', 'Ω']
```

## `insert`

```python
list.insert(i, x)
```

Adds single item at index.

```python
a_list = ['a', 'b', 'c']
a_list.insert(2, [1, 2])  # ['a', 'b', [1, 2], 'c']
```
