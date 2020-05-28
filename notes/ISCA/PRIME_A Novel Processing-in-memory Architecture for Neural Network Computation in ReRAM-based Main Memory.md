**Paper title:**

PRIME: A Novel Processing-in-memory Architecture for Neural Network Computation
in ReRAM-based Main Memory

**Publication:**

ISCA’16

**Problem to solve:**

Processing-in-memory (PIM) is a promising solution to address the “memory wall”
challenges, but prior proposed PIM architectures focus on putting additional
computation logic in or near memory, which are manufacture unfriendly and
high-cost.

**Major contribution:**

1.  The paper proposes a novel PIM architecture for efficient NN computation
    built upon ReRAM crossbar arrays, called PRIME, processing in ReRAM-based
    main memory. PIRME contains a portion of memory arrays (full function
    subarrays) that can be configured as NN accelerators or as normal memory on
    demand.

2.  The paper designs a set of circuits and microarchitecture to enable the NN
    computation in memory, and achieve the goal of low area overhead by careful
    design.

3.  The paper proposes an input and synapse composing scheme to overcome the
    precision challenge.

4.  The paper develops a software/hardware interface that allows software
    developers to configure the full function subarrays to implement various
    NNs.

**Lessons learnt:**

Together with ISAAC, this paper is among the first pioneer works that proposes
ReRAM-based CNN accelerator.

PRIME utilizes the memory arrays themselves for computing instead of adding
logic to memory, which obviates memory cell redesign and has low area overhead,
low cost and friendly manufacture. It is a novel PIM solution to accelerate NN
applications, which enjoys the advantage of in-memory data movement, and also
the efficiency of ReRAM based computation.

Experimental results show that, compared with a state-of-the-art neural
processing unit design(DaDianNao), PRIME improves the performance by ∼2360× and
the energy consumption by ∼895×, across the evaluated machine learning
benchmarks.
