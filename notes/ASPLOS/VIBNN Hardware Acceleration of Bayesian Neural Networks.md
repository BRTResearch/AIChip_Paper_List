**Paper title:**

VIBNN: Hardware Acceleration of Bayesian Neural Networks.

**Publication:**

ASPLOS’18

**Problem to solve:**

Frequent usage of Gaussian random variables in this process requires a properly
optimized Gaussian Random Number Generator (GRNG). The high hardware cost of
conventional GRNG makes the hardware implementation of BNNs challenging.

**Major contribution:**

1.  RAM-based Gaussian (pseudo) random number generators: RAM-based Linear
    Feedback Gaussian Random Number Generator (RLF-GRNG), which is inspired by
    the properties of binomial distribution and linear feedback logics.

2.  Wallace Gaussian (pseudo) random number generators: the Bayesian Neural
    Network-oriented Wallace Gaussian Random Number Generator.

3.  Accelerator architecture on FPGA: To achieve high scalability and efficient
    memory access, they propose a deep pipelined accelerator architecture with
    fast execution and good hardware utilization. Experimental results
    demonstrate that the proposed VIBNN implementations on an FPGA can achieve
    throughput of 321,543.4 Images/s and energy efficiency up to 52,694.8
    Images/J while maintaining similar accuracy as its software counterpart.

RAM-based Linear Feedback Gaussian Random Number Generator method is capable of
approximating a Gaussian distribution when the sample size is large enough.
Importantly, it can be effectively implemented using RAM with compact additional
logics for indexing and computing. The Wallace method relies on the property
that the linear combinations of Gaussian random numbers are still Gaussian
distributed. The linear combinations are achieved through multiplying a vector
of Gaussian random numbers x by a Hadamard matrix H: x ′ = H × x. This approach
does not require multiplication operations. In Wallace algorithm, the original
elements in x are randomly chosen from the pool, and after multiple loops of
transformations, the newly generated random numbers are written back to random
positions in the pool to replace the original elements. In this way, the size of
the pool keeps constant.

**Lessons learnt:**

BNN is a mathematical model, instead of a specific type of neural network
structure. Therefore, the design principles of VIBNN are orthogonal to the
optimization techniques on convolutional layers in previous works, and can be
applied to CNNs and RNNs as well.
