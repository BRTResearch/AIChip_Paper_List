**Paper title:**

AccPar: Tensor Partitioning for Heterogeneous Deep Learning Accelerators

**Publication:**

HPCA’20

**Problem to solve:**

-   Chip specialization returns less benefit as the accelerators are approaching
    the ultimate accelerator wall. It is unlikely to further achieve
    fine-grained optimizations on a single accelerator.

-   Only a few of the existing DNN accelerators are designed for training. Among
    these designs, strict constraints are often applied to the models that can
    be supported.

-   The exploration of solutions for an array of heterogeneous accelerators with
    various computation capacity and network bandwidth is lacked.

**Major contribution:**

-   Proposed a principled and systematic method, AccPar, of determining the
    tensor partition among heterogeneous accelerator arrays.

-   The proposed method includes 2 parts, the first one is a cost model,
    including communication cost model and computation cost model. The second
    one is partition algorithm, which could search more space, could take
    communication cost and bandwidth into consideration, and could handle
    multiple paths in DNN.

**Lessons learnt:**

DNN training specialized accelerators are not as hot as inference specialized
accelerators in both industry and academia. In most realistic situations, GPUs
are applied to accelerate DNN training, and the remaining part is using TPUs.
Compared to the various inference accelerators, training accelerators still have
a long way to go.
