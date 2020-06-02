**Paper title:**

DianNao: A Small-Footprint High-Throughput Accelerator for Ubiquitous
Machine-Learning

**Publication:**

ASPLOS’14

**Problem to solve:**

While most accelerators focus on optimizing computational primitives,
inefficient memory transfers can potentially void the throughput, energy or cost
advantages of accelerators. The paper aims to build an accelerator for CNN and
DNN which minimizes the memory transfers and perform them as efficiently as
possible.

**Major contribution:**

1.  A synthesized (place & route) accelerator design for large-scale CNNs and
    DNNs, the state-of-the-art machine learning algorithms.

2.  The accelerator achieves high throughput in a small area, power and energy
    footprint.

3.  The accelerator design focuses on memory behavior, and measurements are not
    circumscribed to computational tasks, they factor in the performance and
    energy impact of memory transfers.

The paper first analyses the character of components in modern DL algorithms
including DNN and CNN layers, and introduces pseudo-code of dense, convolution
and pooling layers optimized for tiling. A large DNN or CNN can be divided into
tiles, and data can be reused across tiles. To meet the require of large
networks, the paper introduces its accelerator design of an input buffer for
input neurons (NBin), an output buffer for output neurons (NBout), and a third
buffer for synaptic weights (SB), connected to a computational block (performing
both synapses and neurons computations) which we call the Neural Functional Unit
(NFU), and the control logic (CP).

NFU, the computation unit, are design for tiles using Ti inputs and generating
To outputs. The NFU directly pipelined 3 standard stages in neural network
layers: multiplications, sum and activate function in 16 bits.

Rather than cache, the DianNao use buffer for all data including inputs, outputs
and weights. The locality of data is exploited explicitly, and DMA is used to
deal all transfer.

Experiments are carried out on several well-known networks, and speed up and
energy saving are measured.

**Lessons learnt:**

It is the first few works that address AI accelerator hardware design and opens
the new era of AI architecture. The importance of memory hierarchy architecture
in accelerator design, which is well-known now as the main bottleneck.
