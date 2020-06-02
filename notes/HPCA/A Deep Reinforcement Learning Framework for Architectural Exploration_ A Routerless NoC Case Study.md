**Paper title:**

A Deep Reinforcement Learning Framework for Architectural Exploration: A
Routerless NoC Case Study

**Publication:**

HPCA’20

**Problem to solve:**

There are chances in architecture design space exploration using reinforcement
learning. And the author uses Routerless NoC as the study case to show their
reinforcement learning method.

1.  Machine learning developments leverage deep reinforcement learning to
    provide improved design space exploration. This capability is particularly
    promising in broad design spaces, such as network-on-chip (NoC) designs.

2.  Design challenges for routerless NoCs include efficiently exploring the huge
    design space (easily exceeding 1012) while ensuring connectivity and wiring
    resource constraints. This makes routerless NoCs an ideal case study for
    intelligent design exploration.

**Major contribution:**

1.  Fundamental issues are identified in applying deep reinforcement learning to
    routerless NoC designs, including: Specification of States and Action,
    Quantification of Returns, Functions for Learning, Guided Design Space
    Search.

2.  An innovative deep reinforcement learning framework is proposed and
    implementation is presented for routerless NoC design with various design
    constraints. The framework and NN provided are in the paper.

3.  Cycle-accurate architecture-level simulations and circuit-level
    implementation are conducted to evaluate the design in detail.

4.  Broad applicability of the proposed framework with several possible examples
    is discussed, including: 3d-NoC design, optimizing connections between CPUs
    or stacked memories, optimizing NoCs in domain-specific accelerators like
    TPU and Eyeriss.

**Lessons learnt:**

1.  There are chances using NN to optimize the architecture and the more regular
    the architecture is, easier to design the machine learning method.

2.  The whole system design space exploration using the similar method perhaps
    is still challenging and not explored.

3.  Above all, this paper is the combination of computer architecture and
    reinforcement learning. So, we could check if there are other effective
    reinforcement learning method to perform in AI accelerator design space
    exploration.
