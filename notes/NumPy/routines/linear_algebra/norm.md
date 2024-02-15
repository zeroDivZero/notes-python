# `norm`

Returns 1 of 8 different matrix norms, or 1 of infinite vector norms, depending on `ord` param.

```python
numpy.linalg.norm(x, ord=None, axis=None, keepdims=False)
```

## Params

* `x`: array_like
  * Input array. If `axis` `None`, `x` must be 1-D or 2-D, unless `ord` `None`. If both `axis` and `ord` `None`, **2-norm** of `x.ravel` returned.
* `ord`: {non-zero int, inf, -inf, 'fro', 'nuc'}, optional
  * Order of norm. inf means NumPy's `inf` object.
* `axis`: {`None`, int, 2-tuple of ints}, optional.
  * If integer, specifies axis along which to compute vector norm (`axis=1` row-wise, `axis=0` column-wise). If 2-tuple, specifies 2-D axes to compute matrix norm. `None` means either vector norm (when `x` is 1-D) or matrix norm (when `x` is 2-D) returned.

* `keepdims`: bool, optional
  * `True` means axes normed over are left in result as dimensions with size one, result will broadcast correctly against original `x`.

## Returns

* `n`: float or `ndarray`
  * Norm of matrix or vector.
