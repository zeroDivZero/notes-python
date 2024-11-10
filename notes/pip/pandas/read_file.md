# READ FILE

Pandas provides functions to read file data as `DataFrame`. Supported formats include csv, excel, sql, json, etc. Each function starts with prefix `read_`.

```python
student_records = pd.read_csv('data/students.csv')
transportation_expenses = pd.read_excel('finance/expenses.xlsx', sheet_name='Transportation')
```
