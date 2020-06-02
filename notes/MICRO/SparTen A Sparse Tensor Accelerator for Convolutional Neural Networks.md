**Paper title:**

SparTen: A Sparse Tensor Accelerator for Convolutional Neural Networks
**Publication:**

MICRO’19

**Problem to solve:**

A recent fully-sparse architecture, called Sparse CNN (SCNN), supports two-sided
sparsity to improve performance and energy over dense architectures. In
contrast, previous architectures except SCNN, being semi-sparse, do not provide
this support. However, SCNN has two shortcomings.

1.  Inefficient sparse microarchitecture: Sparse vector-vector dot product, a
    key primitive in sparse CNNs, requires finding non zero elements in matching
    positions in two sparse vectors and accessing those elements – an inner join
    with the position as the key and a single value field. SCNN avoids the inner
    join by performing a Cartesian product capturing the relevant
    multiplications. However, SCNN’s approach incurs several considerable
    overheads and is not applicable to non unit-stride convolutions.

2.  Load Imbalance: exploiting reuse in sparse CNNs fundamentally causes
    systematic load imbalance not addressed by SCNN.

**Major contribution:**

1.  SparTen’s microarchitecture achieves efficient inner join for full sparsity
    instead of avoiding the inner join like SCNN. Thus, SparTen avoids SCNN’s
    Cartesian-product overheads. Further, SparTen employs clustered,
    asynchronous compute units to handle sparsity.

2.  To address load imbalance across the computer units of a cluster, SparTen
    employs an offline software scheme, called greedy balancing (GB), which has
    two variants: a software-only one (GB-S) and a software-hardware hybrid
    (GB-H). GB-S groups the filters by density at the granularity of whole
    filters whereas GB-H’s grouping is at a finer granularity (e.g., 128
    elements) for better balance than GB-S. SparTen efficiently achieves both
    filter reuse and load balance.

**Lessons learnt:**

SparTen’s simplicity, efficiency, and high performance make it an attractive
architecture for sparse matrix computations.
