# BOOLEAN OPERATORS

Compares Boolean value(s) and evaluates to single Boolean value.

## Binary Operators

`and`, `or` each operates on two Boolean values.

```python
nice = sugar and spice
question = to_be or not_to_be
```

## Unary Operator

`not` operates on only one Boolean value.

```python
keep_playing = not is_game_over
triple_negatives = not not not True
```

## Mix with Comparison Operators

```python
precedence = 2 + 2 == 4 and not 2 + 2 == 5 and 2 * 2 == 2 + 2  ## True
```

After math and comparison operators, `not` first, then `and`, and `or` last.
