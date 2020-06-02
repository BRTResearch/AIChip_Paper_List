**Paper title:**

A Network-Centric Hardware/Algorithm Co-Design to Accelerate Distributed
Training of Deep Neural Networks

**Publication:**

MICRO’18

**Problem to solve:**

Find a way to reduce the communication cost caused by gradients and weights
updating across the nodes in the distributed network.

1.  Training a modern real-world DNN costs long time.

2.  Although distributed training method could largely reduce the time cost,
    there is a large of fraction spent on communicating weights and gradients
    over the distributed network.

**Major contribution:**

1.  A novel gradient compression technique, which focuses on the compression of
    floating-point values in the range between -1.0 and 1.0 such that it
    minimizes the precision loss while offering high compression ratio.

2.  An in-network accelerator architecture is provided in the paper.

3.  A gradient-centric distributed training algorithm to maximize the benefits
    of the in-network acceleration is provided.
