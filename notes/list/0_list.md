# `list`

Holds ordered sequence of arbitrary objects, can change size dynamically.

## Create and Access

```python
empty_list = []

a_list = [2.718, 'hello', True, 123, None, [7, 8, 9]]
print(a_list[1])  # hello
print(a_list[5][2])  # 9
```

Index goes backwards. Convenient to use `-1` to get last item (assuming list has at least 1 item).

```python
print(a_list[-1])  # [7, 8, 9]
# IndexError if list empty

print(a_list[-3])  # 123
```

## Length

```python
spam = ['cat', 'dog', 'elephant']
print(len(spam))  # 3
```

## Item Existence

```python
'hola' in ['hello', 'nihao', 'hola', 'konichiwa']  # True
greetings = ['hello', 'nihao', 'hola', 'konichiwa']
'howdy' in greetings  # False
'hello' not in greetings  # False
'cat' not in greetings  # True
```

### `index`

```python
list.index(x[, start[, end]])
```

Similarly, can use method `index()` to get index of value. First index if there're duplicates. `ValueError` if not in list.

```python
greetings.index('nihao')  # 1
greetings.index('hi')  # ValueError
```

## Assign Item (Replace)

```python
a_list[3] = False  # [2.718, 'hello', False, 123, None, [7, 8, 9]]
```
