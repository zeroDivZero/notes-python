# SLICE

Creates new list.

```python
a_list = [2.718, 'hello', True, 123, None, [7, 8, 9]]

print(a_list[1:3])  # ['hello', True]
print(a_list[1:-1])  # ['hello', True, 123, None]

print(a_list[:3])  # [2.718, 'hello', True]
print(a_list[3:])  # [123, None, [7, 8, 9]]

print(a_list[:-5])  # [2.718]
print(a_list[:-6])  # []; anything more negative also empty list

b_list = a_list[:]  # creates copy of a_list
```
