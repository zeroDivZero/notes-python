# `list`

Holds ordered sequence of arbitrary objects, can change size dynamically.

## Create and Access

```python
empty_list = []

a_list = ['a', "example", True, 123, [7, 8, 9]]
print(a_list[1])  # example
```

Index goes backwards. Convenient to use `-1` to get last item (assuming list has at least 1 item).

```python
print(a_list[-1])  # [7, 8, 9]
# IndexError if list empty

print(a_list[-3])  # True
```

## Assign Item (Replace)

```python
a_list[2] = False
print(a_list)  # ['a', "example", False, 123, [7, 8, 9]]
```
