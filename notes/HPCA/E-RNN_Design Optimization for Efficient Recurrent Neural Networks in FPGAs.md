**Paper title:**

E-RNN: Design Optimization for Efficient Recurrent Neural Networks in FPGAs

**Publication:**

HPCA’19

**Problem to solve:**

ESE (ESE: Efficient speech recognition engine with sparse LSTM on FPGA) uses a
weight pruning based compressed RNN model but suffers from irregular network
structure after pruning. The second work C-LSTM (C-LSTM: Enabling efficient LSTM
using structured compression techniques on FPGAs) mitigates the irregular
network limitation by incorporating block-circulant matrices for weight matrix
representation in RNNs, thereby achieving simultaneous model compression and
acceleration. A key limitation of the prior works is the lack of a systematic
design optimization framework of RNN model and hardware implementations,
especially when the block size (or compression ratio) should be jointly
optimized with RNN type, layer size, etc.

**Major contribution:**

1.  ADMM-based training: At software level, they use ADMM-based training for
    deriving block-circulant matrix-based RNN representation. ADMM-based
    training is compatible with recent progress in stochastic gradient descent,
    which is not supported in the training method of C-LSTM. ADMM-based training
    provides an effective means to deal with the structure requirement in weight
    matrices, thereby enhancing accuracy and training speed.

2.  Hardware design: At hardware level, we propose a systematic design framework
    and hardware optimization using HLS, to achieve alternative designs for
    RNNs, and to limit the design range and accelerate the design exploration.
    The systematic framework also works for other DNN designs targeted at FPGAs
    due to the regularity of block-circulant matrix.

**Lessons learnt:**

This paper focuses on block-circulant matrix-based RNN implementations and aim
to mitigate these limitations with target application as Automatic Speech
Recognition. The prior work focus on the efficient implementation of RNN
inference phase given a pre-computed RNN model. They did not provide a
systematic method to perform design optimization. When the block size or degree
of model compression needs to be optimized together with the network size and
different block sizes can be utilized for different parts of a network, a
significant increase in the number of RNN training trials will be needed for
design optimization.
