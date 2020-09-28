**Paper title:**

ExTensor: An Accelerator for Sparse Tensor Algebra

**Publication:**

MICRO’19

**Problem to solve:**

1. The percentage of non-zero elements in tensor kernels ranges from 10-6% to
50%. Many tensor kernels are extremely sparse.

2. Proposed accelerators for sparse liner algebra deal with relatively dense
data (e.g. deep neural network) or specific kernels (e.g. sparse matrix vector
multiply).

3. General purpose platform such as CPUs and GPUs cannot reach peak performance
when accumulating sparse tensor algebra kernels.

**Major contribution:**

They propose the first accelerator for general and sparse tensor algebra called
ExTensor.

The key idea of ExTensor is to find the coordinate intersection between input
tensors and select tensors according to those coordinates to accumulate. Input
tensors are stored in compressed format such CSR or CSF and look up via
metadata.

They propose an architecture to find the coordinates of intersection called the
Coordinate. The input of the Coordinate is subtensors with these coordinates.
Sequencer in the Coordinate is configured by tensor kernel. Sequencer is
responsible for sending Iterate() command required by the tensor kernel to the
Scanner. Scanner consist of a metadata storage and a Finite State Machine (FSM)
to control the storage. Metadata storage receive input coordinates.

When evaluating sparse-sparse problems (both tensors are sparse), Extensor
perform intersection as described previously. When evaluating a sparse-dense
problem, intersection is degenerate as all coordinates of the sparse operand are
effectual and those coordinates are used (as positions) to access the values of
the dense operand. For dense-dense, intersection is disabled.

Finally, Compared with MKL, SPMSPM(two sparse matrix multiplication) and SPMM(a
dense matrix multiple sparse matrix) speed up 3.4× and 1.3×. Compared with TACO,
TTV, TTM and SDDMM(three tensor kernels) speed up 2.8×, 24.9×, and 2.7×.

**Lessons learnt:**

1. This paper pre-process the dimensions of tiled tensors in tree format, which
guarantees different dimension tensors are send into acceleration in a same
format.

2. The core of the paper is to find out whether the coordinates of the two trees
in the input tensor are intersecting.

3. Tensors are broken into tiles in different memory hierarchy.
