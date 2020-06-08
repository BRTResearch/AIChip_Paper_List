**Paper title:**

Multi-dimensional Parallel Training of Winograd Layer on Memory-Centric
Architecture

**Publication:**

MICRO’18

**Problem to solve:**

This paper mainly aims at accelerating training for CNN in synchronous
computing, where input batch is distributed across the multiple workers.
However, there is limiting scalability in moderate batch size due to the
communication time.

**Major contribution:**

1.  Propose a novel multi-dimensional parallel training (MPT) of Winograd domain
    convolution that exploits both data and intra-tile (or element-wise)
    parallelism available in Winograd domain.

2.  To efficiently support communication among workers with MPT, this paper
    proposes a 2D organization of worker with hybrid topology that consists of a
    ring topology for collective communication in data parallelism while a high
    connectivity topology is used for tile transfer.

3.  This paper proposes dynamic clustering that enables optimal configuration of
    workers to balance the two different types of communication (weight gradient
    and tile transfer) in the MPT architecture.

4.  This paper proposes prediction of activation in the spatial domain neurons
    from the quantized values of Winograd domain data, without accuracy loss, to
    reduce bandwidth needed for tile gathering.

**Lessons learnt:**

1.  Combine Winograd algorithm and multi-dimensional parallel training (MPT) to
    accelerate the DL training.

2.  Apply the 3D stacked memory and the scalable near-data processing (NDP)
    architecture to increase the bandwidth of data access.

3.  It is commonly high-effectivity to ameliorate speed, accuracy, energy
    consumption or other target by skillfully applying dynamic and predicting
    ways according corresponding data and computation laws.
