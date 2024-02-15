# BROADCAST

Describes how NumPy treats arrays with different shapes during arithmetics. Idea is to broadcast smaller array across larger array so they have compatible shapes.

Provides means of vectorizing array operations so looping occurs in C instead of Python, without making needless data copies and usually leads to efficient implementations. In some cases may lead to inefficient memory usage that slows computation.

Simple example:

```python
a = np.array([1.0, 2.0, 3.0])
b = 2.0
a = a * b  # array([2.,  4.,  6.])
```

`b` *stretched* from scalar to 1x3 vector. Even more efficient than explicitly creating `b` as 1x3 vector because less memory moved around during multiplication.

## Example

Calories from carbs, proteins, and fats from 100g of different foods:

![Food Calories](/assets/NumPy/broadcast-example-cals.png)

To calculate % of cals in each food:

![Broadcast Example](/assets/NumPy/broadcast-example-code.png)

`reshape()` in example not necessary, but cheap operation, good for explicitness.

## General Principle

In arithmetic operation, if larger array is *m x n*, and smaller array is *1 x n* or *m x 1*, smaller array is copied *m* (vertically) or *n* (horizontally) times to match shape of larger array.
