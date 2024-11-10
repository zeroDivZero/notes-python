# WRITE FILE

```python
df.to_excel('students.xlsx', sheet_name='Grades', index=False)
```

Set `index=False` to avoid writing row index labels in file.

Similar to reading files, multiple versions of `to_` methods to write in different formats.
