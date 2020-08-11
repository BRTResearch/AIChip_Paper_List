**Paper title:**

vDNN: Virtualized Deep Neural Networks for Scalable, Memory-Efficient Neural
Network Design

**Publication:**

MICRO’16

**Problem to solve:**

The motivation behind vDNN is based on the following three key observations: 1)
DNNs trained via stochastic gradient-descent (SGD) are designed and structured
with multiple layers; 2) the training of these neural networks involves a series
of layerwise computations, the order of which is statically fixed and repeated
for millions to billions of iterations throughout the entire training process;
and 3) even though the GPU can, at any given time, only process a single layer’s
computation (due to the layer-wise computational characteristics of SGD-based
DNN training), popular ML frameworks adopt a network-wide memory allocation
policy because DNN training requires the intermediate feature maps of all the
layers in the network to be backed up in GPU memory for gradient updates. In
other words, existing memory management schemes overprovision the memory
allocations to accommodate the usage of the entire network layers, even though
the GPU is only using a subset of this allocation for the layer-wise
requirements. The goal of vDNN is to conservatively allocate GPU memory for the
immediate usage of a given layer’s computation so that the maximum and average
memory usage is drastically reduced, allowing researchers to train larger
networks.

**Major contribution**

This work is the first to present a detailed, quantitative analysis on GPU-based
DNN training, as opposed to recent literature targeting energy-efficient
accelerators for DNN inference.

This work is the first that provides an in-depth characterization study on the
memory access characteristics of DNNs and their effect on the GPU memory system
from an architectural perspective.

This work identifies the key limitations of current ML frameworks’ memory
management policies as they require the network-wide memory usage of the target
DNN to monolithically fit within the physical capacity of the GPU. It
demonstrates this by showing that existing frameworks fail in training 6 out of
the 10 studied DNNs when their memory allocation size (14 GB to 67 GB) exceeds
the GPU memory budget (12 GB in NVIDIA’s Titan X).

This paper proposes, implements, and evaluates a runtime memory manager called
vDNN that virtualizes the memory usage of neural networks across CPU and GPU
memories. The vDNN solution reduces the average GPU memory usage of these 6
memory hungry networks by 73% to 98%, allowing them to be trained on a single
Titan X card. Compared to a hypothetical, oracular GPU containing enough memory
to hold the entire DNN, vDNN incurs 1% to 18% performance overhead.

**Lessons learnt**

With the fact that the memory requirement per individual layer is substantially
smaller than what is actually provisioned with the baseline, network-wide memory
allocation policy, vDNN adopts a sliding-window based, layer-wise memory
management strategy in which the runtime memory manager conservatively allocates
memory from its memory pool for the immediate usage of the layer that is
currently being processed by the GPU. Intermediate data structures that are not
needed by the current layer are targeted for memory release to reduce memory
usage.
