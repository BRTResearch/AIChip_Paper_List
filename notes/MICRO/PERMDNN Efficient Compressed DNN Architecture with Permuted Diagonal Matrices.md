**Paper title:**

PERMDNN: Efficient Compressed DNN Architecture with Permuted Diagonal Matrices

**Publication:**

MICRO’18

**Problem to solve:**

1. Current network sparsification method generates DNNs whose structure is
highly irregular and weak regularity, which incurs significant overhead due to
indexing irregular sparse weight matrix.

2. The compress ratio of DNN sparsification is usually uncontrollable and DNN
sparsification approaches cause large training overhead.

3. Representing the network with structured matrices can overcome drawbacks of
irregularity. CIRDNN utilizes circulant matrix to compress DNN.

4. CIRDNN requires high-cost arithmetic computation because the training and
inference algorithm of CIRDNN is based on FFT. Moreover, the compression ratio
is determined by the length of FFT.

5. CIRDNN processes input in the frequency domain, which loses the sparsity in
time domain.

**Major contribution:**

They propose PREMDNN that represents weight matrices in block-permuted diagonal
matrix structure. PREMDNN targets for FC layers. It can handle the inference and
training of FC layers. In CONV layers, they impose the permuted diagonal
structure on the input channel and output channel dimensions of the weight
tensor. The compression ratio of DNN is block size for the permuted diagonal
weight matrix. They also explain the effectiveness of using permuted diagonal
matrix in outline.

They design the PREMDNN architecture for inference task. They implement a 32-PE
design using CMOS 28nm technology. Compared with EIE, PERMDNN achieves 3.3× ∼
4.8× higher throughout, 5.9× ∼ 8.5× better area efficiency and 2.8× ∼ 4.0×
better energy efficiency on different workloads. Compared with CIRCNN, PERMDNN
achieves 11.51× higher throughput and 3.89× better energy efficiency.

**Lessons learnt:**

1. The crucial idea of the paper is to use mathematical characteristic to
simplify the layout in SRAM and index computation.

2. They represent DNN models in a structured way to make implement of hardware
easier.
