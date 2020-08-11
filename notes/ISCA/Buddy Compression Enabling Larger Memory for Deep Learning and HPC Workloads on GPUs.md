**Paper title:**

Buddy Compression: Enabling Larger Memory for Deep Learning and HPC Workloads on
GPUs

**Publication:**

ISCA’20

**Problem to solve:**

GPUs offer orders-of-magnitude higher memory bandwidth than traditional CPU-only
systems. But, their memory capacity tends to be relatively small and can not be
increased by the user.

Applications with large memory footprints must: (i) scale out to many GPUs for
capacity purposes (inefficient resource utilization), (ii) explicitly
orchestrate data movement between the host CPU and the GPU to stay within device
memory limitations (adding algorithmic complexity), or (iii) rely on off-GPU
memory accesses or Unified Memory to automatically oversubscribe device memory
(limiting performance). Thus, we need to explore memory compression as a
solution to this challenge.

**Major contribution:**

Provide an in-depth analysis of the data of representative GPU workloads and
derive insights for effective GPU compression.

Introduce the first design to use general-purpose compression to increase the
memory capacity of GPUs. Buddy Compression does not require any additional data
movement as the compressibility of the data changes.

Buddy Compression achieves 1.9x compression and performs within 2% of an ideal,
high-memory-capacity GPU.

Present a case study on DL training to understand the benefits and trade-offs of
using Buddy Compression.

**Lessons learnt:**

The target workloads: High Performance Computing (HPC) and Deep Learning (DL).
