**Paper title:**

Scalpel: Customizing DNN Pruning to the Underlying Hardware Parallelism

**Publication:**

ISCA’2017

**Problem to solve:**

1.  The sparsity of pruned networks often leads to a performance decrease in DNN
    computation. Sparse weight matrices lose the regular structure of dense
    matrices, and sparse matrix multiplication needs extra computation to decode
    the sparse format. The reduction in model size can, therefore, make up for
    the computation inefficiencies of sparse matrix multiplication. However, the
    reduction in execution time is still much lower than the computation
    reduction.

2.  For CPUs, the effect of weight pruning varies for different networks and
    depends on the computation breakdown between fully-connected and
    convolutional layers. For fully-connected layers, weight pruning can improve
    performance because the total memory footprint is critical to matrix-vector
    multiplication. But for convolutional layers that perform matrix-matrix
    multiplication, the matrix data will be reused multiple times, and there is
    limited benefit from the memory footprint reduction. Therefore, the
    inefficiencies inherent in the sparse matrix format will hurt the
    performance of convolutional layers on CPUs

3.  In addition to the performance decrease, another challenge for weight
    pruning is that a significant amount of data is necessary to record the
    sparse matrix structure. Each nonzero weight needs one extra column index to
    record its position. This extra overhead reduces the impact of weight
    pruning across all hardware platforms.

**Major contribution:**

1.  We demonstrate that DNN weight pruning is not a panacea, but rather its
    impact is closely coupled to both the structure of the network
    (fully-connected vs. convolutional layers) as well as the data-parallel
    structure of the target hardware. The blind application of traditional
    weight pruning often results in performance loss, hence a closer examination
    of this topic is warranted. We propose Scalpel that creates a pruned network
    that is customized to the hardware platform that it will execute. Scalpel
    provides a method to improve the computation speed and reduce the model
    sizes of DNNs across processors ranging from microcontrollers to GPUs with
    no accuracy loss.

2.  SIMD-aware weight pruning is introduced as a refinement to traditional
    weight pruning. It puts contiguous weights into groups of size equal to the
    SIMD width. Extra data for recording the sparse matrix format is reduced
    along with providing higher utilization of SIMD units.

3.  A new method, node pruning, is proposed to compress the DNN model by
    removing redundant nodes in each layer. It does not break the regular
    structure of DNNs, thus avoiding the overheads of sparsity caused by
    existing pruning techniques. We compare the performance of Scalpel to prior
    DNN pruning techniques across three hardware platforms: microcontroller, CPU
    and GPU.
