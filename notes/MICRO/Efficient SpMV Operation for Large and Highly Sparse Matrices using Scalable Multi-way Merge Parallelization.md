**Paper title:**

Efficient SpMV Operation for Large and Highly Sparse Matrices using Scalable
Multi-way Merge Parallelization

**Publication:**

MICRO’19

**Problem to solve:**

Efficient SpMV operation on large problem like working set exceeds on-chip
storage is severely constrained due to strong dependence on limited amount of
fast random access memory to scale. Additionally, unstructured matrix with high
sparsity poses difficulties as most solutions rely on exploitation of data
locality.

**Major contribution:**

1.  **Novel merge parallelization scheme**: A novel radix pre-sorter based
    scalable multi-way merge parallelization scheme that provides high
    throughput to saturate extreme bandwidth of 3D stacking technology, thus
    fully utilize off-chip bandwidth.

2.  **Scale for larger problems**: enable Two-Step SpMV to scale for larger
    problems without signiﬁcantly increasing on-chip fast memory requirement

3.  **Meta-data compression technique**: Variable Length Delta Index (VLDI) can
    signiﬁcantly reduce off-chip trafﬁc and improve performance

**Lessons learnt:**

One of the paper’s target is to deal with large workload. During multi-way merge
operation, the records in any particular list are accessed sequentially.
However, in every cycle only one list dequeues a record and the selection of
that list is practically random. For large problems lists will reside in the
off-chip main memory and random accesses will cause poor utilization of off-chip
bandwidth. So they proposed PRaP as a solution to this problem. The idea is to
implement p independent Merge Cores (MCs) where each will only work on records
with certain radix within the keys. For that purpose, each record streamed from
DRAM is passed through a radix based pre-sorter and directed to its destination
MC.
