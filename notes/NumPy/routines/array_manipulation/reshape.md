# `reshape`

Gives new shape to array without changing data.

```python
numpy.reshape(a, newshape, order='C')
```

## Params

* `a`: array_like
  * Array to be reshaped.
* `newshape`: int or tuple of ints
  * New shape should be compatible with original shape. Integer for 1-D array. One dimension can be `-1` -- value inferred from array length and remaining dimensions.
* `order`: {`C`, `F`, `A`}, optional
  * Read/write elements using particular index order. `C` means C-like -- last axis index changing fastest, back to first axis index changing slowest. `F` means Fortran-like -- first index fastest and last slowest. `C` and `F` take no account of array memory layout. `A` means Fortran-like if `a` is Fortran contiguous in memory, C-like otherwise.

## Examples

## Equivalent `ndarray` Method

```python
ndarray.reshape(shape, order='C')
```

Unlike `numpy.reshape`, allows elements of `shape` param passed in as separate args. E.g., `a.reshape(10, 11)` is equivalent to `a.reshape((10, 11))`.
