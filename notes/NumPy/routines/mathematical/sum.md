# `sum`

Sum of array elements over given axis.

```python
numpy.sum(a, axis=None, dtype=None, out=None, keepdims=<no value>, initial=<no value>, where=<no value>)
```

## Params

* `a`: array_like
  * Elements to sum.
* `axis`: `None` or int or tuple of ints, optional
  * Axis or axes along which sum is performed. Default `axis=None` sums all elements. If negative counts from last to first. If tuple of ints, sum performed on all axes in tuple.
* `keepdims`: bool, optional
  * If `True`, reduced axes are left in result as dimensions with size one, result will broadcast correctly against input array.

## Returns

* `sum_along_axis`: `ndarray`
  * Array with same shape as `a`, with specified axis removed.
