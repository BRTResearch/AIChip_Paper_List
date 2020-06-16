**Paper title:**

Compressing DMA Engine: Leveraging Activation Sparsity for Training Deep Neural
Networks

**Publication:**

HPCA’ 18

**Problem to solve:**

Popular deep learning frameworks require users to fine-tune their memory usage
so that the training data of a deep neural network (DNN) fits within the GPU
physical memory. For large DNN models that use more memory than GPU has, prior
work tries to virtualize the memory usage of DNNs, enabling both CPU and GPU
memory to be utilized for memory allocations. However such virtualizing memory
can incur significant performance overheads when the time needed to copy data
back and forth from CPU memory is higher than the latency to perform DNN
computations.

To compress the data transferred between GPU memory and CPU memory is a
promising way to solve the problem, since it can speed up the data transfer with
fix bandwidth.

**Major contribution:**

The paper’s goal is to develop a virtualization solution for DNN training that
satisfies both memory-scalability and high performance. The main contribution is
as follow:

1.  Presenting a compressing DMA engine (cDMA), a general-purpose DMA
    architecture for GPUs that alleviates PCIe bottlenecks by reducing the size
    of the data structures copied in and out of GPU memory.

2.  Several compressing algorithms are discussed and evaluated in different
    networks..

When training DNN, each layer’s activations must be stored for backward
propagation. The widely used ReLU activation function make such activations
sparse, i.e. contain lots of zero, making it possible to be compressed. First,
the proposed cDMA requests the memory controller to fetch data from the GPU
memory at a high enough rate (i.e., effective PCIe bandwidth × compression
ratio) so that the compressed data can be generated at a throughput commensurate
with the PCIe bandwidth. The cDMA copy-engine then initiates an on-the-fly
compression operation on that data, streaming out the final compressed data to
the CPU memory over PCIe. When fetching data from CPU memory to GPU memory, the
decompression is done on-the-fly too.

Run-length encoding compression, zero-value compression which only stores
non-zero values in a batch of activation with corresponding mask, and Zlib
compression which is of great performance and great complexity, are evaluated in
AlexNet, OverFeat, NiN, VGG, SqueezeNet and GoogLeNet, and showing impressive
compression rate, offering an average 2.6× (maximum 13.8×) savings in data
movement on the CPU–GPU communication link.

**Lessons learnt:**

The sparsity of activations can be further explored, relating works exist from
pruning to compression.

This paper focus on large DNNs training, which make using CPU memory reasonable.
