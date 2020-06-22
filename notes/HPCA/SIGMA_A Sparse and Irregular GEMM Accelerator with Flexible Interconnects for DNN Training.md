**Paper title:**

SIGMA: A Sparse and Irregular GEMM Accelerator with Flexible Interconnects for
DNN Training

**Publication:**

HPCA’20

**Problem to solve:**

There are three key requirements for future GEMM engines based on observations.

1.  Flexibility: GEMM engines should be able to efficiently run matrices of
    arbitrary dimensions.

2.  Sparsity Support: GEMM engines need support for unstructured sparsity in
    both weights and activations in order to fully utilize hardware resources.

3.  Scalability: GEMM engines need to scale efficiently for integration into
    different kinds of accelerators. For example, tiny tensor cores in CPUs/
    GPUs to large cores in a future TPU.

Unfortunately, state-of-the-art GPUs and TPUs fare poorly on some of the
requirements.

**Major contribution:**

1.  The paper proposes the microarchitecture of a flexible and scalable GEMM
    accelerator named SIGMA that can handle (a) arbitrary amounts of sparsity,
    (b) arbitrary irregularity in GEMM dimensions, while guaranteeing close to
    full compute utilization.

2.  The paper proposes a novel reduction network, named Forwarding Adder Network
    (FAN), for efficient partial sum accumulation.

3.  Layout implementation of SIGMA for scalability and backend analysis.

**Lessons learnt:**

The details of neural network accelerators still have some concerns. SIGMA shows
5.7× performance speedup over TPU designs for sparse irregular workloads and a
3× performance speedup over other state-of-the-art sparse accelerators.
