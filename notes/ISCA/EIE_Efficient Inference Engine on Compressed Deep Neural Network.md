**Paper title:**

EIE: efficient inference engine on compressed deep neural network

**Publication:**

ISCA‘16

**Problem to solve:**

Large DNN models are very powerful but consume large amounts of energy because
the model must be stored in external DRAM. Fetching weights from DRAM is two
orders of magnitude more expensive than ALU operations, and dominates the
required power.

**Major contribution:**

1.  To efficiently operate on compressed DNN models, the paper proposes EIE, an
    efficient inference engine, a specialized accelerator that performs
    customized sparse matrix vector multiplication and handles weight sharing
    with no loss of efficiency

2.  The paper describes a method of both distributed storage and distributed
    computation to parallelize a sparsified layer across multiple PEs, which
    achieves load balance and good scalability.

**Lessons learnt:**

It is the first accelerator for space and weight sharing neural networks. And it
is also the first accelerator that exploits the dynamic sparsity of activations
to save computation.

Compared with CPU (Intel i7-5930k) GPU (GeForce TITAN X) and mobile GPU (Tegra
K1), EIE achieves 189×, 13× and 307× acceleration, while saving 24,000×, 3,400×
and 2,700× energy, respectively.
