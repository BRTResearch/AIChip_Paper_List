**Paper title:**

Cambricon-X: An Accelerator for Sparse Neural Networks.

**Publication:**

MICRO‘16

**Problem to solve:**

The state-of-the-art NNs are known to be both computationally and memory
intensive, due to the ever-increasing deep structure, i.e., multiple layers with
massive neurons and connections (i.e., synapses). Sparse neural networks have
emerged as an effective solution to reduce the amount of computation and memory
required. Though existing NN accelerators are able to efficiently process dense
and regular networks, they cannot benefit from the reduction of synaptic
weights.

**Major contribution**

This paper proposes a novel accelerator, Cambricon-X, to exploit the sparsity
and irregularity of NN models for increased efficiency. The proposed accelerator
features a PE-based architecture consisting of multiple Processing Elements
(PE). An Indexing Module (IM) efficiently selects and transfers needed neurons
to connected PEs with reduced bandwidth requirement, while each PE stores
irregular and compressed synapses for local computation in an asynchronous
fashion. With 16 PEs, our accelerator is able to achieve at most 544 GOP/s in a
small form factor (6.38 mm2 and 954 mW at 65 nm). Experimental results over a
number of representative sparse networks show that the proposed accelerator
achieves, on average, 7.23x speedup and 6.43x energy saving against the
state-of-the-art NN accelerator.
