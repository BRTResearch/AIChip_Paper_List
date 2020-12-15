**Paper title:**

DUET Boosting Deep Neural Network Efficiency on Dual-Module Architecture

**Publication:**

MICRO’2020

**Problem to solve:**

1.  Deep neural networks have been driving the mainstream of machine learning,
    which leads to the need of efficiency.

2.  Much data falls into the insensitive region of activation function, which
    can be used to boost the inference.

**Major contributions:**

1.  Proposed a dual-module processing method, which computes accurate result for
    sensitive data and computes approximate results for insensitive data.

2.  Design a specialized dual-module architecture to support the acceleration.
    The architecture includes a speculator and an executor. The speculator
    produces approximate results and a switching map to tell the executor which
    data to be skipped.

3.  Proposed adaptive mapping, which reduces the idle time by reordering the
    units.

**Lessons learnt:**

1.  When producing approximate results, it uses random projection for dimension
    reduction, which can be a good way for approximation without great loss. It
    can also apply to other method.
