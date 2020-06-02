**Paper title:**

DaDianNao: A Machine-Learning Supercomputer

**Publication:**

MICRO’14

**Problem to solve:**

The neural network models are getting so large that it can hardly store on chip,
making it unavoidable to access the memory. If most synaptic weights have to
reside in main memory, and if neurons intermediate values have to be frequently
written back and read from memory, the memory accesses become the performance
bottleneck, just like in processors, partly voiding the benefit of using custom
architectures. However, it is possible to imagine a dedicated machine learning
computer composed of multiple chips, each chip containing specialized logic
together with enough RAM that the sum of the RAM of all chips can contain the
whole neural network, requiring no main memory. The paper aims to propose such a
supercomputer design.

**Major contribution:**

Based on DianNao’s computaion unit NFU and relating buffer SB, DaDianNao
proposed a supercomputer design with distributed memory, and suitable for
multi-board connection. By tightly interconnecting these different chips through
a dedicated mesh, one could implement the largest existing DNNs, achieve high
performance at a fraction of the energy and area of the many CPUs or GPUs used
so far. Due to its low energy and area costs, such a machine, a kind of compact
machine learning supercomputer, could help spread the use of high accuracy
machine-learning applications, or conversely to use even larger DNNs/CNNs by
simply scaling up RAM storage at each node and/or the number of nodes.
(scaleable)

The proposed architecture is composed of interconnected nodes, each containing
computational logic (NFU described in DianNao), eDRAM, and the router fabric.
Each chip also contain a center eDRAM, which can communicate with all nodes on
chips. The weights are stored in the memory of the node using them once possible
to reduce the data movement, and the output result may store in center eDRAM.

Nodes on chip are connected by a classical mesh. All the nodes are connected
through a fat tree which serves to broadcast the input values to each nodes, and
to collect the output values from each nodes. At the center of the chip, there
are two special eDRAM banks, one for input data, the other for output data.
Nodes have their local memory to store intermediate results.

On the higher level, chips are connected with each other using HyperTransport
(HT) 2.0 in 2D mesh.

**Lessons learnt:**

The idea of placing data as near to corresponding computation units as possible
to minimize data transfer is very important.

Mapping the whole network onto chip(s) can largely save time and energy, and
Google’s IPU do the same thing: mapping kernels of a graph onto chips, so that
data transfer between chips and outer memory can be minimized.
