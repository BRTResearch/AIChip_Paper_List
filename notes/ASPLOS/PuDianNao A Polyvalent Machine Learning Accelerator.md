**Paper title**

PuDianNao: A Polyvalent Machine Learning Accelerator

**Publication**

ASPLOS’15

**Problem to solve**

The insight here is that an ML accelerator should be able to support diverse ML
techniques, in order to address needs under different scenarios. There is
significant diversity among existing ML techniques, making it hard to design a
pervasive ML accelerator. The diversity is two-fold. First, different ML
techniques may differ a lot in their computational primitives. This paper takes
two classification algorithms, naïve bayes and k-nearest neighbors (k-NN), as
examples. The most time-consuming part of naive bayes is estimating the
conditional probabilities, but that of k-NN is calculating distances between
instances (each represented as a feature vector). Second, different ML
techniques may differ a lot in their locality properties. For example, a large
number of instances in k-NN may be frequently reused to classify unseen
instances, while each feature (vector component) of an instance is not
frequently reused in naive bayes.

**Major contribution**

First, we thoroughly analyze several representative ML techniques to extract
their key computational tasks and locality properties, which establishes a solid
foundation for the design of ML accelerator.

Second, we design novel functional units to cover common computational
primitives of different ML techniques, as well as on-chip storage that
comprehensively factors in locality properties of different ML techniques.

Third, we present PuDianNao, an accelerator accommodating seven representative
ML techniques and multiple ML scenarios

**Lessons learnt**

1.  The analysis of machine learning algorithm computational primitives and
    locality properties is important and more subtle. In addition to
    computational primitives of the seven algorithms, they also integrate their
    different operators into the accelerator.

2.  Improved emulators, using the cycle-by-cycle C simulator of PuDianNao based
    on C simulator. The entire accelerator architecture, which contains a lot of
    computational primitives and locality properties , is flexible.
