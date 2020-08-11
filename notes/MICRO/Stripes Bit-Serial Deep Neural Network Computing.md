**Paper title:**

Stripes: Bit-Serial Deep Neural Network Computing

**Publication:**

MICRO’16

**Problem to solve:**

The high computation demands of DNNs and the need for higher energy efficiency
motivated special purpose architectures such as the state-of-the-art DaDianNao
(DaDN) which was reported to be up to 330x more energy efficient than a GPU. As
power tends to be the limiting factor in modern high-performance designs, it is
essential to achieve better energy efficiency in order to improve performance
further under the given power constraints.

**Major contribution**

This work presents Stripes (STR), an implementation of a DNN performance
improvement technique that 1) is complementary to existing techniques which
exploit parallelism across computations, while 2) improving energy efficiency,
and 3) enabling accuracy vs. performance trade offs.

STR relies on bit-serial compute units and on the parallelism that is naturally
present within DNNs to improve performance and energy with no accuracy loss. In
addition, STR provides a new degree of adaptively enabling on-the-fly trade-offs
among accuracy, performance, and energy. Experimental measurements over a set of
DNNs for image classification show that STR improves performance over a
state-of-the-art accelerator from 1.30x to 4.51x and by 1.92x on average with no
accuracy loss. STR is 57% more energy efficient than the baseline at a cost of
32% additional area. Additionally, by enabling configurable, per-layer and
per-bit precision control, STR allows the user to trade accuracy for further
speedup and energy efficiency.

**Lessons learnt**

Motivation of STR: 1) Numerical Precision Requirements vary across and within
networks. 3) Precision variability could improve performance. 3) Enabling
accuracy vs. performance trade-offs.
