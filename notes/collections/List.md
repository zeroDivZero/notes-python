# LIST

Stores 0 or more elements at specific indexes. Element accessed by index.

Can contain multiple types.

Mutable.

```python
record = ['Ellis Smith', 16, False, ['A', 'B+', 'A-', 'B', 'A-']]

inventory = ['Sword', 'Boots', 'Bread']
weapon = inventory[0]
inventory[2] = 'Apple'

print(len(inventory))
print(max(inventory))
print(min(inventory))

inventory.append('Potion')
inventory.insert(1, 'Knife')

last_item = inventory.pop()
inventory.remove('Sword')
inventory.clear()
```

## Multi-Dimensional

```python
universe = [[1, 2, 3],
            [1, 2, 3, 4],
            [1, 2],
            [1, 2, 3]]
ninth_world = universe[2][1]
universe.append([1, 2, 3, 4, 5])
universe[1].pop()
```
