# SET

Unordered collection with no duplicate elements.

```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}

print(basket)  # {'orange', 'pear', 'banana', 'apple'}
```

## Create New Set with `set`

Takes iterable (list, tuple, dictionary, etc.).

```python
a = set([1, 1, 2, 2, 3, 3])  # {1, 2, 3}
b = set('abracadabra')  # {'c', 'b', 'a', 'r', 'd'}
```

## Operations

Subtraction: `a - b`.
Union: `a | b`.
Intersection: `a & b`.
XOR: `a ^ b`.
Existence: `10 in a`.

## Comprehension

```python
a = {x for x in 'abracadabra' if x not in 'abc'}  # {'r', 'd'}
```
