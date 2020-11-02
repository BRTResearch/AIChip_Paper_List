**Paper title:**

TensorDIMM: A Practical Near-Memory Processing Architecture for Embeddings and
Tensor Operations in Deep Learning

**Publication:**

MICRO’19

**Problem to solve:**

1. Emerging DL(Deep Learning) algorithms demand both high memory capacity and
bandwidth, limiting the types of applications that can be deployed under
practical constraints. The model size of embedding layers (typically several
hundreds of GBs) far exceeds the memory capacity of GPUs on recommender systems.

2. The solution is store the entire embedding lookup table inside the
capacity-optimized, low-bandwidth CPU memory and deploy the application by only
CPU or by a hybrid CPU-GPU approach, leaving significant performance loss
compared by GPU-only version.

3. The reason of performance loss: 1) the embedding vectors are read out using
the low-bandwidth CPU memory, incurring significant latency overheads compared
to when the embeddings are read out using the bandwidth-optimized GPU memory. 2)
the low computation throughput of CPUs can significantly slowdown the
computation-heavy DNN execution step when solely relying on CPUs, whereas the
hybrid CPU-GPU version can suffer from the latencies in copying the embeddings
from CPU to GPU memory over the thin PCIe channel.

**Major contribution:**

They present a vertically integrated, hardware/software co-design to tackle
memory problem.

They present TensorDIMM, which is based on commodity buffered DIMMs but further
enhanced with near memory processing (NMP) units customized for key DL tensor
operations, such as embedding gathers and reductions. The NMP units in
TensorDIMM are designed to conduct embedding gathers and reduction operations
“near-memory” which drastically reduces the latency in fetching the embedding
vectors and reducing them, providing significant improvements in effective
communication bandwidth and performance.

They propose a custom tensor ISA and runtime system that provides scalable
memory bandwidth and capacity expansion for embedding layers. Our proposal
entails 1) a carefully designed ISA tailored for DL tensor operations
(TensorISA), 2) an efficient address mapping scheme for embeddings, and 3) a
runtime system that effectively utilizes TensorDIMMs for tensor operations.

They aggregate a pool of TensorDIMM modules as a disaggregated memory node
(henceforth referred to as TensorNode) in order to provide scalable memory
capacity expansion. A key to their proposal is that TensorNode is interfaced
inside the NVLINK-compatible, GPU-side high-bandwidth system interconnect. The
benefits of interfacing TensorNode within the GPU interconnect is that by
storing the embedding lookup tables inside the TensorNode, GPUs can copy in/out
the embeddings much faster than the conventional CPU-GPU based approaches.

Their vertically integrated solution provides an average 6.2−15.0× and 8.9−17.6×
speedup in inference time compared to the CPU-only and hybrid CPU-GPU
implementation of recommender systems, respectively.

**Lessons learnt:**

In emerging DL application, embedding layers is the most memory-intensive
algorithm and may take up much execution time in the whole DL workload in
datacenter.
