**Paper title:**

SpArch: Efficient Architecture for Sparse Matrix Multiplication.

**Publication:**

HPCA’20

**Problem to solve:**

Generalized Sparse Matrix-Matrix Multiplication (SpGEMM) is a ubiquitous task in
various engineering and scientific applications. However, inner product based
SpGEMM introduces redundant input fetches for mismatched nonzero operands, while
outer product based approach suffers from poor output locality due to numerous
partial product matrices. Inefficiency in the reuse of either inputs or outputs
data leads to extensive and expensive DRAM access.

**Major contribution:**

The paper proposes SpArch, a domain-specific accelerator to jointly optimize
input and output data reuse. The major contributions are as follows:

1.  Pipeline the multiply stage and the merge stage with a comparator
    array-based highly parallelized merger.

2.  Use matrix-condensing to condense the first input matrix, reducing the
    number of partial matrices by three orders of magnitude.

3.  Develop a Huffman tree scheduler that provides a near-optimal merge order of
    partial matrices and reduces the DRAM traffic.

4.  A row prefetcher that achieves near-optimal buffer replacement policy for
    the second input matrix and resolves the increased DRAM read induced by
    matrix condensing.

On real-world datasets from SuiteSparse, SNAP and rMAT, SpArch achieves 4×, 19×,
18×, 17×, 1285× speedup, and 6×, 164×, 435×, 307×, 62× energy saving over
OuterSPACE, MKL, cuSPARSE, CUSP and ARM Armadillo.
