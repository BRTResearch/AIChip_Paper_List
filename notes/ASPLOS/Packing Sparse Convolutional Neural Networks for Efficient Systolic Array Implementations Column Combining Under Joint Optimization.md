**Paper title:**

Packing Sparse Convolutional Neural Networks for Efficient Systolic Array
Implementations: Column Combining Under Joint Optimization

**Publication:**

ASPLOS’19

**Problem to solve:**

1. The remaining nonzero weights in pruned DNN models are distribute in an
unstructured manner, which may not efficiently utilize the regular structure of
systolic arrays.

2. The weights set to zero after pruning still occupy systolic cells in order to
maintain synchronization across all cells in the array during matrix
multiplication.

**Major contribution:**

They propose column combining algorithm for packing sparse CNNs with
unstructured sparsity into a denser format for efficient systolic array
implementations. In a weight matrix, they select some columns into a column
group and combine them in a single column. For columns which have more than one
nonzero weights in a row, they choose the one with the largest magnitude.

They develop a systolic array system for column combining. The systolic array
comprises of many cells. Cells are based on bit-serial MACs. Each MAC process
8-bit input data and 8 bit weight. The weights are stationed in cells and input
data and output partial sum flow into systolic array. To handle high-precision
accumulation, a cell consists of more than one MACs process accumulation
concurrently. As weights in combined columns may contain more than one channels,
the input data and partial sum should contain more channels. They design
multiplexed input cells for solution.

They present analysis and empirical evidence on the superior performance of our
column combining approach against prior arts under metrics such as energy
efficiency (3x) and inference latency (12x).

**Lessons learnt:**

1. They combine unstructured weight matrix into a denser weight matrix for
efficient hardware implement.

2. MAC process concurrently in a systolic array cell can compute
higher-precision accumulation.
