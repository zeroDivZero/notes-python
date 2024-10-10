# SLICE

Creates new list.

```python
a_list = ['a', "example", True, 3.14, [7, 8, 9]]

print(a_list[1:3])  # ['example', True]
print(a_list[1:-1])  # ['example', True, 3.14]

print(a_list[:3])  # ['a', "example", True]
print(a_list[3:])  # [3.14, [7, 8, 9]]

print(a_list[:-5])  # ['a']
print(a_list[:-6])  # []; anything more negative also empty list

b_list = a_list[:]  # creates copy of a_list
```
