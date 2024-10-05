# EXCEPTION HANDLING

Even syntactically correct code can have execution errors known as *exceptions*. Example Python exceptions: `ZeroDivisionError`, `NameError`, `TypeError`.

If not handled, program ends with error message and stack trace. To programmatically handle selected exceptions, use `try except`:

```python
while True:
  try:
    x = int(input('Please enter a number: '))
    break
  except ValueError:
    print('Oops! That was no valid number. Try again...')
```

Can handle multiple exceptions simultaneously by naming exceptions tuple in `except` clause:

```python
except (RuntimeError, TypeError, NameError):
  pass
```

If need exception object:

```python
except requests.exceptions.RequestException as e:
  print(f'Error: {e}')
```

Can have optional`else` clause to run code when no exception raised:

```python
try:
  f = open(arg, 'r')
except OSError:
  print('cannot open', arg)
else:
  print(arg, 'has', len(f.readlines()), 'lines')
  f.close()
```

## Clean-up Action with `finally`

Optional `finally` clause to run code under all circumstances:

```python
try:
  raise KeyboardInterrupt
finally:
  print('Goodbye, world!')
```
