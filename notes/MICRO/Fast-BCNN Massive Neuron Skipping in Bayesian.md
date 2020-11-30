**Paper title:**

Fast-BCNN: Massive Neuron Skipping in Bayesian Convolutional Neural Networks

**Publication:**

MICRO’20

**Problem to solve:**

BCNN is a method that places probability distributions over models’ weights in
contrast to conventional CNN. It’s implemented by adding a dropout layer after
every convolutional layer of a normal CNN. The problems that exist in the method
is:

1.  The dropout layers have not been studied. They are only added after not that
    important FC layers.

2.  The dropout implementation brought overwhelmed computation loads.

3.  BCNN works inefficiently on high-end platforms like GPU.

**Major contribution:**

1.  Fast-BCNN skips the computations for dropped and unaffected neurons. They
    gives a method that decides if a neuron is considered to be unaffected.

2.  They proposed a parallelism scheme that can maximize the contribution of the
    skipping strategy based on analysis of existing parallel schemes.
