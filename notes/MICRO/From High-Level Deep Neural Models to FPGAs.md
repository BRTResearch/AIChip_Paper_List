**Paper title:**

From High-Level Deep Neural Models to FPGAs

**Publication:**

MICRO’16

**Problem to solve:**

1. FPGAs-based DNN acceleration has a limited on-chip memory size and off-chip
bandwidth.

2. A rigid accelerator for DNNs may not fully utilize the FPGA’s limited
resource for different DNN models.

**Major contribution:**

They develop a framework called DNNWEAVER that automatically generates
accelerator for a given (DNN, FPGA). The DNN model is described in Caffe. Caffe
code will translate into a dataflow ISA proposed by this paper. The ISA is a
dataflow architecture. Each instruction in ISA comprises a unique static ID that
represent a unique instruction that will receive the result. None of the
instructions contain source operands.

They design a hand-optimized template accelerator. DNNWEAVER generates a rigid
accelerator according to the specific DNN model from the template accelerator.
In the template, many PUs connect Data Buffer to receive input feature map. Each
PU many PEs with weight buffer to calculate convolution layer in DNN. In
addition, each PU also comprise normalization unit, pooling unit and lookup
table for activation to produce result of different type of layers in DNN.

They make the PEs read input data row by row and generate partial results rather
than separating input data into PEs to calculate the whole part of output
feature. The partial result is stored in a local FIFO in each PE. Also, they add
a unidirectional link between adjacent PEs to reuse input data. In pooling
layer, they overlap pooling operations with convolution operations in PEs.

They propose a heuristic algorithm to decide number of PEs-per-PU and output
slice of each PU. Due to the fix resource of FPGAs, increasing the number of PE
in each PU decreases the number of PU in the accelerator. Because each PE need
an input data buffer as well as slice size should fit the on-chip memory in PU,
they use an algorithm called Template Resource Optimization search algorithm.
The algorithm search the minimal execution cycles in the specific number of
PEs-per-PU and slice.

**Lessons learnt:**

1. The paper uses search algorithm to decide the variables of scalable template
architecture to suit different DNN models and FPGA platforms.

2. The template architecture optimizes the data access from data buffer by
reducing fetch redundant data and reuses data by adding unidirectional link
between PEs.
