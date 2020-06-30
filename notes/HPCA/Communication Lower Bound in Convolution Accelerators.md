**Paper title:**

Communication Lower Bound in Convolution Accelerators

**Publication:**

HPCA’20

**Problem to solve:**

CNN accelerators often involve a great number of memory accesses. Normally,
communication, but not computation, dominates the energy consumption of a CNN
accelerator. From an energy point of view, current CNN accelerators are
communication dominant. Minimizing the communication, therefore, is the key for
improving the energy efficiency of CNN accelerators.

Data reuse heavily depends on the convolutional dataflow. There are various
approaches to optimize the dataflow: 1) designing an elaborate dataflow, 2)
selecting the best dataflow from several candidates, and 3) design space
exploration (DSE). A fair number of these studies focus on the performance
and/or the energy efficiency of the computational components. Moreover, in most
existing studies, the dataflow is designed based on intuitive/heuristic
analysis, which may not guarantee the optimality.

The paper aims to find the lower bound of data communication of both on-chip and
off-chip under given hardware resources, and to design an accelerator to reach
such lower bound.

**Major contribution:**

The major contributions of the paper are:

1.  Solving a fundamental problem in CNN accelerators: what the lower bound of
    the off-chip communication of a convolutional layer is, if it is implemented
    on a CNN accelerator with a limited on-chip memory. A mathematical
    derivation for this problem is provided.

2.  Demonstrating that convolutions have only one more level of data reuse
    (sliding window reuse) than matrix multiplications (MMs). Based on this
    conclusion, a dataflow which fuses sliding window reuse and a
    communication-optimal MM implementation is elaborated, to minimize the
    off-chip communication.

3.  Proposing a workload and storage mapping scheme such that both GBuf
    communication and Reg communication respectively reach their lower bounds.

4.  A communication-optimal CNN accelerator architecture is proposed, which not
    only reaches the minimum communication, but also can adapt to different
    convolutional layer dimensions with high resource utilization.

The paper first derivation the lower bound of off-chip communication depending
on the red-blue pebble game, a theoretical model to estimate the minimum volume
of data transmission between two levels of memories.

The paper also proposes a CNN accelerator architecture design.

The CNN accelerator is computation dominant and the energy efficiency is close
to the theoretical best value. The proposed dataflow even produces 6.7% less
DRAM access volume than Eyeriss with input compression on VGG-16. Our
implementations (with smaller total and effective on-chip memory capacities)
produce much less GBuf communication than Eyeriss, and the reduction factors are
10.9-15.8x. The large reduction is due to the elimination of data shuffling
between the GBuf and LRegs.

**Lessons learnt:**

This paper provides a systemic and theoretical discussion about optimized memory
accessing in limited hardware resource, taking global buffers (registers) and
local buffers (registers) into considered.
