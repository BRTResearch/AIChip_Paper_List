**Paper title:**

Understanding and Optimizing Asynchronous Low-Precision Stochastic Gradient
Descent

**Publication:**

ISCA’17

**Problem to solve:**

Stochastic gradient descent (SGD) is one of the most popular numerical
algorithms used in machine learning and other domains. Since this is likely to
continue for the foreseeable future, it is important to study techniques that
can make it run fast on parallel hardware. In this paper, we provide the first
analysis of a technique called Buckwild! that uses both asynchronous execution
and low-precision computation.

**Major contribution:**

In this paper, the DMGC signature will help researcher understanding the
precision within this algorithm firstly. The author summarize the quantized
methods in precision and defined this signature rule. Secondly, the DMGC
signatures were effective to hand-optimize the implementation in speedup.

This paper identifying lots of models with a wide variety of size proposed a
roofline, to estimate the performance of an algorithm by classifying it as being
either bandwidth-bound or communication-bound. It also exploited the effect of
mini batch size and prefetching on communication-bound solving scheme.

This paper propose four software optimized ways, which can be used to improve
the performance of BUCKWILD! SGD:

This paper suggest two hardware enhancements, obstinate cache and low-precision
computation on the FPGA.
