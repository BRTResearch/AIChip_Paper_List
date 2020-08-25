**Paper title:**

Prediction based Execution on Deep Neural Networks

**Publication:**

ISCA’18

**Problem to solve:**

1. Many output neurons are ineffectual even if the zero-removal technique has
been applied. These ineffectual output neurons (iEON) cannot pass their value to
the subsquent layer.

2. Cnvlutin focuses on the convolution layer of DNN and cannot reduce the memory
access overhead of fully-connected (FCN) layers.

3. The existence of Max-pooling (MaxP) layer reduces the amount of zeros, and
this can stultify the zero-removal technique of Cnvlutin.

**Major contribution:**

They propose a DNN execution model to predict iEON to avoid the futile
computations called uniform serial processing element (USPE). Furthermore, they
make a scale-out design for USPE to improve the processing throughout.

The key idea of the paper is to split DNN training processing into 2 part,
prediction stage and execution stage. They use high bits of input and the whole
weight to predict whether the output neuron is effectual or not. Meanwhile, the
prediction is part of the whole computation. The executor obtain the final value
by adding its result with prediction part result. Because of the different
bitwidth between low-bit and high-bit, parallel multiplier cannot handle
prediction stage and execution stage at the same time. To reuse the hardware,
they change the parallel multiplier into serial multiplier.

This paper investigates that the combination of weight splitting and input
splitting get higher performance. Input splitting can achieve higher speedup and
weight splitting has an advantage of memory access efficiency.

This paper also makes a scale-out design. There exist two opportunities for data
sharing. The first is filter sharing. The USPEs in one row can share the same
filter data. The second is input sharing. All the USPE in one column share the
same input data.

In the execution stage, the scale-out design for prediction stage is not
suitable. It may cause idleness of USPE array. Although without sharing the
input data and filter can solve the problem, the memory access capacity is
challenged. The authors investigate that the number of the efficient output
neurons (EONs) in each output feature maps (OFMs) is nearly the same and can be
calculated based on the network architecture parameters. Also, all the EONs in
the same OFM correspond to the same filter. Therefore, they choose filter
sharing for Max-pooling and input data are not shared. As for ReLU, the
summation of the EONs with the same coordinate across different OFMs is nearly
the same. Hence, they choose input data sharing.

The architecture is implemented in FPGA. The design achieve 2.5× speedup and
1.9× energy-efficiency on average over the traditional accelerator. In addition,
it can improve Cnvlutin and Stripes by 1.9× and 2.0× on average.
