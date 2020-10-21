**Paper title:**

Fused-Layer CNN Accelerators

**Publication:**

MICRO’16

**Problem to solve:**

By processing each layer to completion, the accelerator designs must use
off-chip memory to store intermediate data between layers, because the
intermediate data are too large to fit on chip. This paper tries to reduce the
data transfer between off-chip memory and on-chip processing units.

**Major contribution:**

1.  Rather than processing each CNN layer to completion before proceeding to the
    next layer, it is possible to restructure the computation such that multiple
    convolutional layers are computed together as the input is brought on chip,
    obviating the need to store or retrieve the intermediate data from off-chip
    memory.

2.  This paper develops a novel CNN evaluation strategy that breaks away from
    the commonly accepted practice. By modifying the order in which the original
    input data are brought on chip, changing it to a pyramid-shaped multi-layer
    sliding window.

3.  To explore recomputing or storing, they compare the methods on real-world
    networks using the same procedure. Considering the two approaches for
    AlexNet, they find that a relatively small amount of storage can allow reuse
    to replace a relatively large amount of recomputation. For example, when
    fusing the first two layers of AlexNet, the recompute method would need to
    perform an extra 678 million multiplications and additions to avoid off-chip
    transfer, an 8.6x increase in the overall number of arithmetic operations.
    On the other hand, the reuse model only requires 55.86KB of additional
    on-chip storage to avoid the same off-chip transfer without performing
    additional computation. For typical CNNs targeting computer vision
    applications, such as the AlexNet and VGG networks they consider in this
    paper, the costs of the recomputation model are prohibitive, while the
    storage costs of the reuse model are relatively small. Based on this
    analysis, in the remainder of this work, they focus solely on the reuse
    model.

4.  As the number of fused layers increases, the benefits (reduction of data
    transferred to and from DRAM) increase, but so do the costs (on-chip memory
    required or redundant computation performed). Thus, there is a tradeoff
    between the costs incurred and the benefits. Given a CNN, we examine this
    tradeoff space by exploring the different possible ways to partition the
    network. They consider all possible locations to start and stop pyramids and
    evaluate the above model for each set of possibilities.

**Lessons learnt:**

This paper split the NN execution into several pyramids so as to reduce data
transfer. For deep neural networks, it’s hard to consider all possible fusing
schemes (i.e., fuse two layers or three layers) so as to find an optimized
scheme.
