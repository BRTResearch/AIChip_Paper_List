**Paper title:**

Scale-Out Acceleration for Machine Learning

**Publication:**

MICRO’15

**Problem to solve:**

1.  the community is developing mostly single-node accelerators for a variety of
    applications, including machine learning. However, there is a gap between
    scale-out systems and accelerators due to the lack of solutions that enable
    distributed acceleration at scale. Moreover, it is not enough to just design
    and integrate accelerators independent from algorithms and programming
    interfaces。

2.  Reusing the traditional stack for scale-out acceleration is inadequate as
    the entire computing stack is designed and optimized merely for CPUs, which
    were the sole processing platform up until recently.

3.  Furthermore, as technology is scaled, modern FPGAs and ASICs can harbor an
    ample amount of resources, whose effective utilization necessitates
    rethinking accelerator design paradigms.

**Major contribution:**

1.  How to enable scale-out acceleration of many ML algorithms, yet disengage
    programmers from hardware design. To tackle this challenge, CoSMIC leverages
    a combination of two theoretical insights: (1) a wide range of learning
    algorithms are stochastic optimization problems, solved using a variant of
    gradient descent ; (2) differentiation is a linear mathematical operator,
    and thus the gradient over a set of data points can be calculated as an
    aggregated value over the partial gradients computed in parallel for each
    point.

2.  How to design customizable accelerators that exploit the large capacity of
    advanced process technologies. CoSMIC offers a novel Multiple-Instruction
    Multiple-Data (MIMD) multi-threaded template architecture that divides the
    resources across multiple instances of the learning algorithm as independent
    threads. The last layer of CoSMIC customizes this template and generates the
    final accelerator by striking a balance between the number of threads
    running on the chip and the resources assigned to each thread CoSMIC’s
    backend compiler minimizes data movement by mapping operations to where
    their operands are located.
