# SHAPE

```python
a = np.random.randn(5)
```

`a.shape` is `(5,)`, not row or column vector, but **rank 1 array**. `a.T` is exactly same as `a`, so `np.dot(a, a.T)` produces single scalar instead of matrix.

Explicitly specify shape:

```python
a = np.random.randn(5, 1)
```

`a.shape` then becomes `(5, 1)`.

Can use assertion to check shape:

```python
assert(a.shape == (5, 1))
```

Reshape if necessary:

```python
a.reshape(5, 1)  # or np.reshape(a, (5, 1))
```
