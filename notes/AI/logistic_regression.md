# LOGISTIC REGRESSION

## Sigmoid

```python
import numpy as np

def sigmoid(x):
    return 1 / (1 + np.exp(-x))
```

## Sigmoid Gradient (Derivative)

```python
def sigmoid_derivative(x):
    s = sigmoid(x)
    return s * (1 - s)
```

## Reshape

```python
def image2vector(image):
    """
    Argument:
    image -- numpy array of shape (length, height, depth)

    Returns:
    vector of shape (length*height*depth, 1)
    """
    return image.reshape(-1, 1)
```

## Normalize

Divide each row vector by norm. Gradient descent converges faster.

```python
def normalize_rows(x):
    """
    Argument:
    x -- numpy matrix of shape (n, m)

    Returns:
    normalized (by row) numpy matrix
    """

    x_norm = np.linalg.norm(x, axis=1, keepdims=True)
    return x / x_norm
```

## Softmax

Normalizing function used when alg needs to classify two or more classes.

![Softmax](/assets/AI/softmax.png)

```python
def softmax(x):
    """
    Argument:
    x -- numpy matrix of shape (m,n)

    Returns:
    numpy matrix equal to softmax of x, of shape (m,n)
    """
    x_exp = np.exp(x)
    x_sum = np.sum(x_exp, axis=1, keepdims=True)
    return x_exp / x_sum
```

## L1 Loss

![L1 Loss](/assets/AI/l1-loss.png)

Used to evaluate model perf. Bigger loss means greater difference between predictions from true values.

```python
def L1(yhat, y):
    """
    Arguments:
    yhat -- vector of size m (predicted labels)
    y -- vector of size m (true labels)

    Returns:
    L1 loss value
    """
    return np.sum(np.abs(y - yhat))
```

## L2 Loss

![L2 Loss](/assets/AI/l2-loss.png)

```python
def L2(yhat, y):
    """
    Arguments:
    yhat -- vector of size m (predicted labels)
    y -- vector of size m (true labels)

    Returns:
    L2 loss value
    """
    diff = y - yhat
    return np.dot(diff, diff)
```
